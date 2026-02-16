---
id: "005-flows"
title: "Flows & Business Logic"
type: doc
subtype: core
status: complete
sequence: 5
tags: [user-flow, journey, business-logic, conversion]
---

# Flows & Business Logic

> This document outlines key user journeys and business logic flows for the Wimmer Consulting website.

## Visitor to Lead Conversion Path

This flow describes the primary path for converting an anonymous visitor into a qualified lead.

1.  **Entry**: Visitor lands on a service page (e.g., `/services/erp-dynamics-365`) from an organic search result.
2.  **Engagement**: Visitor reads about the challenges of legacy ERPs and the benefits of Microsoft Dynamics 365.
3.  **Consideration**: Visitor clicks on an internal link to a related case study, reading how a similar company benefited from the service.
4.  **Action**: Impressed by the expertise and results, the visitor navigates to the `/kontakt` page via the main navigation CTA.
5.  **Conversion**: Visitor fills out the contact form to schedule a free consultation.
6.  **Confirmation**: Upon successful submission, the visitor sees an inline success message and the form is cleared.

## Contact Form Submission Flow

This flow details the technical and user-facing steps of a form submission.

- **Initial State**: User is on the `/kontakt` page with a blank form.
- **User Action**: User fills in their name, email, and message and clicks "Senden".
- **Transition (Client-side)**: JavaScript validation runs. If any required field is empty or the email format is invalid, an error message is displayed next to the respective field, and submission is blocked.
- **Transition (Server-side)**: If validation passes, the form data is sent via POST request to a serverless function.
- **Processing**: The function validates the data again, checks the honeypot field for spam, and sends a formatted email to `office@wimmer-edv.at`.
- **Success State**: The function returns a `200 OK` status. The website displays a success message (e.g., "Vielen Dank! Ihre Nachricht wurde gesendet.") to the user.
- **Error State**: If the function fails, it returns an error status. The website displays a generic error message (e.g., "Ein Fehler ist aufgetreten. Bitte versuchen Sie es später erneut.").

## Blog Discovery Flow

This flow illustrates how a user discovers and engages with blog content.

1.  **Entry**: User lands on the homepage (`/`).
2.  **Navigation**: User clicks on "Blog" in the main navigation.
3.  **Listing Page**: User arrives at `/blog`, browses the list of recent articles, and uses the category filter to find posts related to "IT-Sicherheit".
4.  **Post Selection**: User clicks on a compelling title, such as "Cybersicherheit für den Mittelstand: 5 Sofortmaßnahmen".
5.  **Reading**: User reads the blog post content on the article's unique page (`/blog/cybersicherheit-fuer-den-mittelstand`).
6.  **Next Action**: At the end of the post, the user sees a CTA prompting them to learn more about related services and clicks the link to the `/services/it-sicherheit` page.

## Newsletter Signup Flow

- **Initial State**: User is reading a blog post or is in the website footer.
- **User Action**: User enters their email address into the newsletter signup form and clicks "Abonnieren".
- **Transition**: A client-side script validates the email format. On success, the email is sent to an API endpoint for the email marketing service.
- **Success State**: The form displays an inline confirmation message, such as "Erfolgreich angemeldet!"
- **Error State**: If the email is invalid or the API call fails, an error message is shown.