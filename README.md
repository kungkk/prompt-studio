# Prompt Studio v1.0

Standalone, dependency-free AI Prompt Builder with eight categories, live preview, clipboard copy, text export, reset, optional verification and reusable sections. No external scripts, cookies, analytics, data persistence or network requests are included.

## Run locally
Open `index.html` in a modern browser. Alternatively, serve locally with `python -m http.server 8000` and open `http://localhost:8000`.

## Deploy for Notion
1. Review this application's source to ensure it meets your requirements and contains no secrets.
2. Choose a static HTTPS host. Publish `index.html` as a static site **only after approving the host's public/private access policy**.
3. Check that host permits framing from `https://www.notion.so` and `https://*.notion.site` as applicable. Avoid X-Frame-Options: DENY/SAMEORIGIN or CSP frame-ancestors rules that block Notion. Host-specific compatibility needs testing.
4. Test the URL in a private browser session to understand who can access it. A private Notion page does not protect a public app URL.
5. In the existing Notion page, type `/embed`, paste the approved HTTPS URL and resize the block. Test inputs, preview, Copy and Save .txt inside Notion. Browsers may block clipboard or download functions in frames.
6. Verify existing Notion page sharing has not changed.

## Current status
Built as a standalone static artifact; **not deployed or embedded**. No Notion permissions were changed.

## Security and limitations
All processing happens in page memory. Prompts are not auto-saved or sent to any service. Clipboard/download require user interaction and may be blocked in some embed contexts. If hosted publicly, visitors can inspect public page source and can access the builder outside Notion. For private app access, deploy behind an appropriately configured authentication/authorization layer and validate iframe and cookie behavior.
