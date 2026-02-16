---
id: "006-design"
title: "Design System"
type: doc
subtype: core
status: complete
sequence: 6
tags: [design, style-guide, branding, ui, ux]
---

# Design System

> This document defines the visual and tonal identity for the Wimmer Consulting brand and website.

## Brand Voice

- **Authoritative, Technical, Professional**: Content should be clear, confident, and precise. It should educate and build trust by demonstrating deep expertise without being overly academic. The tone is that of a trusted advisor and strategic partner.

## Color System

The color palette is modern and professional, designed to convey trust, stability, and innovation.

- **Primary**: `#0056B3` (A strong, trustworthy blue for headlines, buttons, and key interactive elements.)
- **Secondary**: `#6C757D` (A neutral gray for subheadings, secondary text, and borders.)
- **Accent**: `#FF6F00` (A vibrant orange for calls-to-action and highlighting critical information.)
- **Neutral (Text)**: `#212529` (A dark, near-black for body text to ensure high readability.)
- **Neutral (Background)**: `#F8F9FA` (A light off-white for page backgrounds to provide a clean, airy feel.)

## Typography

A combination of a strong sans-serif for headings and a highly readable sans-serif for body text.

- **Heading Font**: Montserrat (Used for all `<h1>` through `<h6>` tags. Bold weights like 600 or 700 are preferred.)
- **Body Font**: Open Sans (Used for paragraphs, lists, and other body content. Regular weight (400) is standard.)
- **Scale**: A modular type scale is used to ensure consistency. (e.g., `h1`: 2.5rem, `h2`: 2rem, `h3`: 1.75rem, `p`: 1rem).

## Spacing System

A 4-point grid system is used for all spacing and layout decisions. All margins, paddings, and gaps are multiples of 4px to maintain visual rhythm (e.g., 8px, 16px, 24px, 32px).

## Component Patterns

- **Buttons**:
  - **Primary**: Solid background (`#0056B3`) with white text. Used for primary CTAs like "Kontakt".
  - **Secondary**: Outlined with a `#0056B3` border and text on a transparent background. Used for secondary actions.
- **Cards**: Used for blog posts and case studies. Feature a subtle border, a drop shadow on hover, consistent padding, and a clear typographic hierarchy.
- **Forms**: Input fields have a light gray border, which turns to the primary blue (`#0056B3`) on focus. Labels are placed above the inputs. Validation messages appear below the field in a distinct color.

## Layout Patterns

The site uses a responsive grid system to adapt to different screen sizes.

- **Desktop Breakpoint**: `1200px+`. Uses a standard 12-column grid with a maximum content width of 1140px.
- **Tablet Breakpoint**: `768px - 1199px`. Content adapts to a single column or a simpler 2-column layout.
- **Mobile Breakpoint**: `< 767px`. A single-column layout is used for all content. The primary navigation collapses into a hamburger menu.