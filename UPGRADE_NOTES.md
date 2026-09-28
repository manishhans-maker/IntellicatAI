# IntellicatAI v8 upgrade pass

This pass intentionally preserves the existing UI/design.

## Fixed

- Aligned AI quota limits across the server and Firestore bootstrap rules:
  - Free: 25 requests / cycle
  - VIP: 150 requests / cycle
  - Founder: 500 requests / cycle
- Fixed the frontend/backend Groq API key field mismatch (`customGroqKey` vs `groqApiKey`).
- Fixed the frontend/backend memory context field mismatch (`userMemoryContext` vs `memoriesContext`).
- Changed frontend quota consumption so a request is counted after a successful generated response instead of before the request starts.
- Added basic SEO metadata, Open Graph/Twitter metadata, canonical URL, JSON-LD WebApplication data, robots.txt, and sitemap.xml.

## Verification

The project dependencies could not be installed in this environment because the package installation timed out. A global TypeScript check was still run; it reported missing installed dependencies/types, but no new syntax error was reported in the modified files.

Before deployment, run:

```bash
npm install
npm run lint
npm run build
```
