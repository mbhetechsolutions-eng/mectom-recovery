# MECTOM SDT Website Recovery Package

Recovered from the live website on 8 September 2026.

## What is included

- `live-snapshot/` — a deploy-ready copy of the current compiled website.
- `live-snapshot/assets/` — the deployed JavaScript and CSS bundles.
- `live-snapshot/public/` — a clean copy of every recovered image, flyer, icon and video for rebuilding the editable project.
- `CURSOR_REBUILD_PROMPT.md` — a complete prompt for Cursor to recreate the maintainable React source project.
- `SITE_CONTENT_AND_STRUCTURE.md` — the pages, wording, prices, forms, contact details, links and behaviour recovered from the website.

The original editable source code cannot be reconstructed byte-for-byte from a production build. However, the live compiled application, its styling and its media have been recovered. The `live-snapshot` folder preserves the current site closely enough to redeploy it immediately, while the Cursor prompt instructs Cursor to recreate clean editable source with the same appearance and content.

## Important live-site issue found

Direct visits to `/about`, `/gallery`, `/blog`, `/courses`, `/contact` and `/enroll` currently return a server 404. The pages work only after the homepage loads and the visitor clicks a navigation link. The included `.htaccess` and `_redirects` files correct this for Afrihost/Apache and Netlify respectively.

## Current technology identified

- React single-page application
- Vite-style production bundle
- Poppins for primary typography
- JetBrains Mono for labels and small technical text
- Web3Forms for enquiry/enrolment delivery
- Responsive desktop and mobile navigation
- HTML metadata, Open Graph, X/Twitter metadata and Schema.org structured data
- WhatsApp floating action button

## Quick recovery options

1. For an immediate backup deployment, upload everything inside `live-snapshot/` to the domain's public web directory.
2. For editable source code, open a new empty folder in Cursor, attach this recovery package, paste `CURSOR_REBUILD_PROMPT.md`, and let Cursor rebuild the React project.

Before production use, configure a fresh Web3Forms access key through an environment variable, replace the placeholder Google Analytics ID, and test both forms.
