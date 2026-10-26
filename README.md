# Kartgen Infotech LLP: frontend demonstration site

Pure frontend, local-only demonstration. No backend, database, API routes, server actions,
authentication, analytics, external services or form submission.

**Stack:** Next.js (App Router), TypeScript, React, Tailwind CSS 4, Lucide React.
All content lives in local TypeScript files under `src/data/`.

## Run locally

```bash
npm install
npm run dev        # http://localhost:3000 (Next picks another port if busy)
```

Checks: `npm run lint`, `npm run typecheck`, `npm run build`.

## The official logo (required step)

The official Kartgen logo was **not** included in the supplied kit and has not been recreated.
Copy the original, unmodified file into `public/brand/` named one of:

`kartgen-logo.svg` · `kartgen-logo.png` · `kartgen-logo.webp` · `kartgen-logo.jpg`

`BrandLogo` (`src/components/layout/BrandLogo.tsx`) then shows it unchanged in the header and footer.
Until then a labeled placeholder is shown. After adding the logo, review the colour tokens in
`src/styles/design-tokens.css` (navy and blue are the kit's starter values).

## Routes

`/` · `/services` · `/services/business-automation` · `/services/websites-digital-platforms` ·
`/services/cloud-technology-optimization` · `/about` · `/work` · `/contact` · custom 404.

## Structure

- `src/data/`: all copy (`site`, `navigation`, `services`, `projects`, `home`, `about`, `contact`)
- `src/components/ui/`: Container, Button, Card, SectionHeading, Badge, Illustration, ServiceIcon
- `src/components/layout/`: Header, MainNavigation, MobileNavigation, Footer, BrandLogo
- `src/components/sections/`: homepage sections
- `src/components/services/`: ServiceCard, ServicePageTemplate (shared by all three service pages), FaqAccordion, RelatedServices
- `src/components/work/`, `src/components/forms/`
- Client Components (`"use client"`) are limited to MainNavigation, MobileNavigation, FaqAccordion, DemoContactForm.

## Content integrity

- No clients, testimonials, metrics, awards or contact details are invented.
- Every project and service example is labeled **Illustrative Concept**.
- Contact details in `src/data/site.ts` are `null` until confirmed; the UI handles that state.
- The contact form validates in the browser only and states that nothing is sent or stored.
