# Kokou Eklou-Agnide — portfolio

A static, responsive portfolio with an original editorial layout and a Couch Trivia Live case study. No build step or backend is required.

## Preview

Open index.html directly, or run `python -m http.server 8081` in this directory and open http://localhost:8081.

## Proxmox hosting

Use an existing Ubuntu/Debian VM or LXC with a web server, or a Docker-enabled VM. Copy this folder to your guest. If Docker Compose is already installed, run `docker compose up -d` here. Open http://GUEST_IP:8081 from your network.

For an existing Caddy or Nginx installation, serve all HTML files, assets/, journal/, and resume.pdf from its web root. The included Caddyfile assumes /srv. Public domain routing and HTTPS should be configured in your existing reverse proxy for the domain you choose; this package does not change your homelab network.

## Editing

- index.html: home page and résumé-based project summaries.
- couch-trivia.html: detailed lead project, including AI-assisted development and last documented status.
- assets/style.css: visual system and responsive styles.
- resume.pdf: public résumé with the phone number removed and an embedded watermark.

The diagram is a custom conceptual illustration, not a screenshot. No project screenshots or unprovided outcome metrics are invented. Every project links to a dedicated overview. The four additional overviews are grounded in the supplied résumé; they do not invent implementation details or results.

Fonts load from Google Fonts, with system fallbacks if unavailable. For a fully offline site, remove the first @import line in assets/style.css or self-host licensed copies of those fonts.

Before publication, confirm your preferred role, project ownership wording, current Couch Trivia status, and contact details. This package has not been deployed to your homelab.

## Portable main page

The main page embeds all five project details and its styles. Project links use native URL fragments and CSS :target, so they work without JavaScript or separate HTML pages. Open index.html in a regular web browser. The standalone case-study pages remain available for direct links.

## CCNA learning journal

The Journal contains collapsible Week 1 and Week 2 entries with previews and full PDF downloads. Extract the entire ZIP before opening index.html. Keep the journal and assets folders beside it so all images and PDFs can load.

For future entries, use journal/entry-template.md to draft notes, then add a new collapsible entry to index.html and place its files in a new week folder under journal/.
