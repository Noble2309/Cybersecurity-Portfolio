# Daniel Jones - Cybersecurity Portfolio

A privacy-conscious static portfolio presenting penetration-testing experience, security research and public project work.

## Release status

This repository contains the production v1.0 release, deployed at [https://cybersecurity-portfolio.noble2309.workers.dev/](https://cybersecurity-portfolio.noble2309.workers.dev/). It includes the personal About section, current interests and credentials, the in-development project placeholder, privacy-conscious Contact copy, and the final accessibility/security baseline.

## Overview

The portfolio uses a technical-editorial design language rather than a stereotypical hacker aesthetic: dark graphite surfaces, restrained blue accents, strong typography, selective monospace detail, custom project emblems and subtle micro-interactions.

The site is intentionally small and dependency-free. Essential content and navigation are available without JavaScript; JavaScript is used only to enhance the mobile navigation and reveal animations.

## Current release

The release includes:

- responsive Home, Projects, About, CV, Contact, Copyright and custom 404 pages;
- a professional portrait and custom SVG artwork for the three featured security projects;
- project case studies with explicit Problem, Approach, Outcome and My Contribution sections;
- selected certifications, current technical interests and a personal Outside of Security section;
- a privacy-sanitised public CV with direct personal contact information removed;
- LinkedIn and GitHub as the only public contact routes, presented as text links;
- keyboard-accessible navigation, visible focus states and reduced-motion support;
- progressive enhancement so core navigation remains available without JavaScript;
- no analytics, tracking, cookies, external fonts or third-party JavaScript;
- restrictive Content Security Policy and supporting browser-security headers for Cloudflare static deployment;
- basic SEO and social-sharing metadata;
- a restrained in-development panel for future project work;
- favicon and robots configuration; and
- all-rights-reserved copyright notices.

## Public projects

1. **Remediation Enablement Framework** - security workflow design and a static reference prototype for structured risk acceptance and retest readiness.
2. **AI Accountability for SOCs** - a sanitised public reconstruction of academic work on AI governance, responsibility assignment and bias testing in security operations.
3. **LLM Prompt Injection Testing Methodology** - an independently rewritten public prompt-injection testing methodology covering direct, indirect, RAG, multimodal, tool and agent-context attack paths.

## Architecture

```text
Browser
  |-- HTML
  |-- CSS
  |-- Vanilla JavaScript (progressive enhancement only)
  |-- SVG assets
  `-- Public CV PDF

No backend
No database
No authentication
No analytics
No cookies
No third-party JavaScript
No external fonts
```

## Security and privacy

The production Cloudflare deployment uses `_headers` to apply a restrictive policy including Content Security Policy, HSTS, clickjacking protection, MIME-sniffing protection, Referrer Policy, Permissions Policy and cross-origin isolation controls appropriate to the static site.

The public source contains no personal email address, telephone number or street address. The downloadable CV is a separately sanitised public version with those details removed.

## Accessibility

The site is designed around WCAG 2.2 AA principles, including semantic document structure, keyboard navigation, visible focus states, a skip link, meaningful link text, sufficient colour contrast, reduced-motion support and no essential interaction that depends solely on hover or JavaScript.

## Repository structure

```text
Cybersecurity-Portfolio/
├── index.html
├── projects.html
├── about.html
├── cv.html
├── contact.html
├── copyright.html
├── 404.html
├── COPYRIGHT.md
├── README.md
├── _headers
├── robots.txt
├── sitemap.xml
├── wrangler.jsonc
├── .assetsignore
└── assets/
    ├── css/
    ├── js/
    ├── images/
    └── documents/
```

## Run locally

From the repository root:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Production deployment

Live site: [https://cybersecurity-portfolio.noble2309.workers.dev/](https://cybersecurity-portfolio.noble2309.workers.dev/)

The site is deployed through Cloudflare Workers Builds from the `main` branch. `wrangler.jsonc` explicitly configures the repository root as the static-asset directory and enables the custom 404 page. `.assetsignore` excludes repository-only metadata from the deployed asset bundle.

## Copyright

Copyright © 2026 Daniel Jones. All rights reserved.

This repository is public for portfolio demonstration and professional review. No open-source licence is granted. See [COPYRIGHT.md](COPYRIGHT.md) for the source-repository notice and `copyright.html` for the styled website notice.
