---
id: "007-technical"
title: "Technical Architecture"
type: doc
subtype: core
status: complete
sequence: 7
tags: [tech-stack, architecture, seo, deployment, performance]
---

# Technical Architecture

> This document provides an overview of the technical stack, strategies, and requirements for the Wimmer Consulting website.

## Technology Stack

The stack was chosen for performance, developer experience, and maintainability.

- **Framework**: Astro 5. A modern static site generator that ships zero JavaScript by default, ensuring excellent performance.
- **Styling**: Tailwind CSS v4. A utility-first CSS framework for rapid UI development and a consistent design system.
- **Language**: TypeScript. For type safety and improved code quality across the project.
- **Deployment**: Vercel. A serverless platform providing seamless deployment, continuous integration from GitHub, and hosting for serverless functions (e.g., for the contact form).
- **Code Repository**: GitHub. For version control and collaboration.

## SEO Strategy

A multi-faceted SEO strategy is in place to drive organic growth.

- **Keyword Strategy**: Content is built around identified keyword clusters: IT Consulting, ERP Systems (Dynamics 365), Cloud & IT Infrastructure, IT Security, and Software Development. Long-tail keywords are targeted via blog posts.
- **Content Strategy**: A blog will be regularly updated with high-quality content addressing the identified content gaps (e.g., modern cloud services, advanced IT security) and targeting specific user pain points. Service pages will be comprehensive and solution-focused.
- **On-Page SEO**: Every page features optimized and unique `<title>` tags, meta descriptions, and a logical heading structure (`<h1>`, `<h2>`, etc.). Images include descriptive `alt` text.
- **Technical SEO**: The site generates an `sitemap.xml`, uses a valid `robots.txt`, and implements `LocalBusiness` and `Service` schema markup using JSON-LD to enhance search engine visibility. All URLs are user-friendly and canonical tags are used to prevent duplicate content issues.

## Performance Targets

Performance is a critical feature of the website.

- **Google Lighthouse Score**: Target a score of 95+ across all categories (Performance, Accessibility, Best Practices, SEO).
- **Largest Contentful Paint (LCP)**: Aim for under 2.5 seconds.
- **Cumulative Layout Shift (CLS)**: Aim for a score of less than 0.1.

## Deployment & Hosting

- **Provider**: Vercel
- **Workflow**: The main branch of the GitHub repository is connected to the Vercel project. Every push to `main` automatically triggers a new production deployment. Pull requests generate unique preview deployments for testing before merging.

## Accessibility Requirements

The website must be accessible to all users, including those with disabilities.

- **Compliance**: The site will adhere to the Web Content Accessibility Guidelines (WCAG) 2.1 at a Level AA conformance.
- **Key Requirements**:
  - All interactive elements must be keyboard-navigable.
  - All images must have appropriate alternative text.
  - Text content must have a contrast ratio of at least 4.5:1 against its background.
  - The site must use semantic HTML to define page structure and meaning.