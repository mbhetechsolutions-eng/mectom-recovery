# Cursor Prompt — Rebuild MECTOM SDT Website

I lost the editable source code for the MECTOM Skills Development and Training website. Rebuild it as a clean, production-ready React application by using the attached recovery package and the deployed reference at `https://www.mectomskillsdevelopment.co.za/`.

The result must match the existing site by at least 90–100% in content, layout, branding, typography, spacing, imagery, animation and responsive behaviour. Do not redesign the brand or replace the recovered wording with generic copy.

## Source of truth

Use these sources in this order:

1. The files inside `live-snapshot/`, especially the current compiled CSS and the running bundle.
2. `SITE_CONTENT_AND_STRUCTURE.md` for all page wording, prices, forms and links.
3. The live site for visual comparison.

## Required stack and project structure

- React with Vite.
- JavaScript or TypeScript; prefer TypeScript if starting clean.
- React Router for client-side routing.
- Reusable components for Header, Footer, PageHero, CTA, WhatsAppButton, BackToTop, CourseCard, SectionHeading and form controls.
- Central data files for courses, testimonials, contact details, social links, partners and gallery media.
- Keep all recovered media in `public/` with their existing filenames so no page references break.
- Use semantic HTML, accessible labels, keyboard-friendly controls and visible focus states.
- The site must be fully responsive and must not create horizontal scrolling.

## Brand and visual rules

- Primary look: bold black/charcoal and white, with coral red `#ff6b6b` as the main accent.
- Additional status/accent colours already present include green `#22c55e`, yellow `#ffd54f`, dark text `#111`/`#1a1a1a`, muted text `#5a6475`, and light greys.
- Use `Poppins` for primary UI and display typography.
- Use `JetBrains Mono` for small labels, categories, stats and technical microcopy where the current site does.
- Preserve the strong editorial/industrial layout, oversized headings, bordered cards, uppercase labels, animated transitions, clean white sections and dark footer.
- Preserve the introductory loading/brand animation, fixed WhatsApp button, sticky navigation, mobile menu, scrolling testimonial treatment and back-to-top control.
- Use the recovered `operator.mp4` video in the homepage hero exactly as the current site does.

## Required routes

- `/` — Home
- `/about` — About Us
- `/gallery` — Gallery
- `/blog` — Blog & Special Offers
- `/courses` — Courses
- `/contact` — Contact Us
- `/enroll` — Enrolment
- A proper Not Found route for unknown URLs

Every route must work when opened directly or refreshed. Add an Apache `.htaccess` fallback for Afrihost and a Netlify `_redirects` fallback.

## Shared header and footer

Header navigation: Home, About Us, Gallery, Blog, Courses, Contact Us, and a coral `Enroll Now` button. Use `logo.png` and clearly show the active route.

Floating WhatsApp URL: `https://wa.me/27732712822`.

Footer content:

- “Skills Development & Training — QCTO Accredited.”
- Address: 33 Plantation Road, Old Industrial, Tzaneen, Limpopo 0850
- Phone numbers: 015 004 0390, 079 423 3878, 073 271 2822
- Email: mectomskills@gmail.com
- TikTok: `https://www.tiktok.com/@mectom.pty.ltd?_r=1&_t=ZS9753BYibDoi`
- Instagram: `https://www.instagram.com/mectom.pty.ltd`
- Facebook: `https://www.facebook.com/mectom.pty.ltd`
- X: `https://x.com/mectomsdt`
- Copyright: © 2026 MECTOM Skills Development and Training (Pty) Ltd. All rights reserved.
- Credit: Engineered by MbheTech Solutions and Masinge IT Solutions, with links to `https://mbhetech.co.za/` and `https://masingeitsolutions.co.za/`.

## Pages and content

Implement every section and all exact wording described in `SITE_CONTENT_AND_STRUCTURE.md`. Do not omit any testimonial, course, price, FAQ, table, partner, gallery image, promotional flyer or call-to-action.

## Forms

Contact form fields: name, email, subject and message.

Enrolment form fields: full name, email, phone, course selection, optional message, ID/passport upload, proof of qualifications upload, and optional CV upload.

Submit through Web3Forms. Store the key in `VITE_WEB3FORMS_ACCESS_KEY`; do not hard-code a secret into source. Display sending, success and error states. Reset on successful submission. The enrolment form must also provide a mailto button so supporting documents can be emailed to `mectomskills@gmail.com`.

## SEO and metadata

- Preserve per-page titles and descriptions.
- Use the canonical production domain consistently: `https://www.mectomskillsdevelopment.co.za/`.
- Add Open Graph and X/Twitter metadata.
- Add Organization, LocalBusiness, EducationalOrganization, Course and Breadcrumb structured data where relevant.
- Remove the placeholder Google Analytics ID `G-XXXXXXXXXX`. Only enable analytics when a real ID is supplied through `VITE_GA_MEASUREMENT_ID`.
- Create `robots.txt` and `sitemap.xml` for all public routes.

## Quality checks before finishing

1. Run the production build and fix all errors.
2. Test every route directly, including refreshes.
3. Test desktop, tablet and mobile layouts.
4. Verify all recovered images and the hero video load locally.
5. Test validation and status feedback on both forms without submitting test spam.
6. Confirm phone, email, WhatsApp and social links.
7. Confirm there are no console errors, broken assets or placeholder values.
8. Keep all content in editable data/component files rather than a single oversized component.

After completion, provide a concise summary of the project structure, setup commands, environment variables and Afrihost deployment instructions.
