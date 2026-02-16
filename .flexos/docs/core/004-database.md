---
id: "004-database"
title: "Database & Data Model"
type: doc
subtype: core
status: complete
sequence: 4
tags: [database, data-model, schema, astro, collections]
---

# Database & Data Model

> This document specifies the data schemas and sources for the Wimmer Consulting website, which is built on Astro and uses content collections for data management.

## Content Collections

As a static site built with Astro, the primary data is managed via Markdown-based content collections stored within the Git repository. No traditional database is required.

### Blog Collection (`/src/content/blog`)

This collection stores all blog posts. Each post is a Markdown file with the following YAML frontmatter schema:

```yaml
# The main title of the blog post. (Required, String)
title: "Microsoft Dynamics 365 vs. Legacy ERP: Wann lohnt sich der Wechsel?"

# A brief, one-sentence summary for listings and SEO. (Required, String)
description: "Erfahren Sie, wann der richtige Zeitpunkt für ein KMU ist, von einem alten ERP-System auf das moderne Microsoft Dynamics 365 umzusteigen."

# The publication date of the article. (Required, Date)
pubDate: "2024-07-15"

# A list of relevant tags for filtering and categorization. (Optional, Array of Strings)
tags: ["erp", "dynamics 365", "digitalisierung", "kmu"]

# Path to the hero image for the post. (Optional, String)
image: "/images/blog/dynamics-vs-legacy.jpg"

# The author of the post. (Optional, String)
author: "Wimmer Consulting"
```

### Case Studies Collection (`/src/content/case-studies`)

This collection stores client success stories with the following schema:

```yaml
# The name of the client or project. (Required, String)
client: "Musterfertigung GmbH"

# A headline for the case study. (Required, String)
title: "Prozessoptimierung in der Produktion durch ERP-Migration"

# A one-line summary for the case study listing page. (Required, String)
description: "Wie wir der Musterfertigung GmbH halfen, ihre Effizienz um 25% zu steigern durch die Implementierung von Dynamics 365 Business Central."

# The industry of the client. (Required, String)
industry: "Fertigung"

# A list of services provided in the project. (Required, Array of Strings)
services: ["ERP Implementierung", "Prozessoptimierung", "Cloud-Migration"]

# Path to a relevant project image or client logo. (Optional, String)
image: "/images/case-studies/musterfertigung.jpg"

# The date the case study was published. (Required, Date)
pubDate: "2024-06-20"
```

## Form Submissions

### Contact Form

The contact form does not connect to a database directly. Submissions are handled by a serverless function on the hosting platform (Vercel) which validates the data and forwards it as an email to a designated company address.

**Submission Schema**:
- **name**: `String`, required
- **email**: `String`, required, must be valid email format
- **message**: `String`, required
- **honeypot**: `String`, optional, for spam prevention

## API Integrations

- **Map Provider**: An embedded map on the contact page may use an API (e.g., Google Maps) to display the company location. This is a client-side integration and does not involve data storage.