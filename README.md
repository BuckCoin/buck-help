# BUCK Wallet Help Center

Official English-language documentation for https://help.buck.red/.

## Structure

- `index.html`: topic directory and safety notice.
- `getting-started/index.html`: introduction and installation documentation status.
- `security-backup/index.html`: privacy precautions and backup/recovery documentation status.
- `synchronization/index.html`: general introduction and documentation status.
- `troubleshooting/index.html`: safe issue descriptions and documentation status.
- `faq/index.html`: frequently asked questions.
- `404.html`: error page with root-relative links for nested missing URLs.
- `assets/css/help.css`: responsive BUCK 2.0 theme.
- `assets/img/buck-logo.png`: unchanged official branding asset.
- `CNAME`: production domain; preserve byte-for-byte (no trailing newline).

## Branding provenance

Logo copied unchanged from `BuckCoin/buckcoin.github.io`, `img/logo-light.png` on `main`, Git blob SHA `08676fca3d8c276fe6ade3f7d9f2cbb4c1a93f53`. The official source `index.html` references that asset. The dark wordmark is displayed on a mint panel for readability. Theme: background `#0C1118`, cards `#14232B`, accent `#8EDEC0`, primary text `#FFFFFF`.

## Maintenance

Edit the static HTML and shared CSS directly. No build step, JavaScript, forms, analytics, external fonts, or runtime dependencies are required. Navigation is repeated on every page; keep it consistent and set `aria-current="page"` for the current topic. Ordinary pages use relative paths; the error page uses root-relative paths for this custom domain.

All public documentation must remain in English. Verify technical procedures against current official BUCK Wallet documentation before adding them, recording the source and applicable version in the maintenance review. Do not infer current supported releases from historical website links. Installation, downloads, backup formats, recovery methods, and synchronization commands are intentionally not specified until verified. Never request seed phrases, private keys, passwords, or wallet backup files.

Preview from the repository root with `python3 -m http.server 8000`. Before integrating changes, validate HTML and CSS, all local links and assets, desktop/mobile layouts, keyboard navigation, and text/focus contrast. Review external links and content for sensitive information and unverified procedures. Compare `CNAME` against the baseline with `git diff --exit-code <baseline> -- CNAME`. Publish only after all required checks pass. Do not change DNS or GitHub Pages settings as part of documentation maintenance.
