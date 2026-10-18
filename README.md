# EW — English Wallah (starter project)

This is a larger, responsive website starter for the English Wallah learning project.

## Included
- Responsive landing page and navigation
- Selection for all 28 Indian states
- Help-language selection and English/Hindi interface toggle
- 100 quiz entries loaded from `questions.json`
- Quiz categories, scoring, answer feedback and restart
- Live-class section placeholders
- Local-only demo panel to add questions
- PWA manifest and service-worker caching starter

## Run locally
For a quick preview, open `index.html` in a browser. For full question loading and PWA service-worker testing, use a local web server because browsers restrict `fetch()` and service workers on `file://` pages. If Python is installed, open a terminal in this folder and run:

    python -m http.server 8000

Then open `http://localhost:8000`.

## Publish on the web
Upload the project files to a GitHub repository and enable GitHub Pages, or use another static host. Keep `index.html`, `questions.json`, `manifest.webmanifest`, `sw.js`, and `icon.svg` in the published root. After publication, test the live HTTPS URL on mobile and desktop.

## Important: not yet a production service
This is a front-end starter, not a complete production platform:
- The Admin demo is not protected and does not save data to a server.
- Quiz entries after the first 20 are practice variations; replace them with reviewed, original questions before public launch.
- Language selection is a preference only; full professional translations for all listed languages are not implemented yet.
- Live classes need actual official YouTube Live/meeting links, schedules, moderation and safeguarding.
- Real accounts, role-based owner/admin/teacher controls, student progress, database, backups and secure authentication need a backend.
- Do not store passwords, personal student data or secrets in HTML, JavaScript, GitHub Pages or this local demo.
- This package does not itself publish an Android app to Google Play. For Play Store release, build/test an Android app or Trusted Web Activity around the deployed HTTPS website, prepare store assets and privacy disclosures, and complete the current Google Play Console requirements. A developer account and user approval are required.

## Recommended production architecture
- Public website: HTTPS static front-end
- Backend/API: managed backend with secure authentication and database
- Roles: owner, teacher, student; enforce permissions on the server
- Classes: scheduled public/private streams with approved links and moderation
- Content: original questions reviewed by educators, translation review by fluent speakers
- Safety/privacy: privacy policy, terms, contact details, reporting/moderation and data deletion process
