<p align="center">
  <img src="assets/logo-on-light.png" alt="Trainerdate" width="360">
</p>

# trainerdate.com

Marketing website for Trainerdate, a marketplace and operating system for personal training. People find trainers, gyms, studios, and academies on a map, read verified reviews, and book. Trainers run their business from one app: booking, payments and packages, client messaging, programs, progress tracking, and paid communities. Hosted on GitHub Pages at **[trainerdate.com](https://trainerdate.com)**.

## Pages

Every page leads with what the platform does and what that gets each audience.

| File | Audience and content |
|------|----------------------|
| `index.html` | Everyone: the four audiences, how booking works, platform capabilities, AI principles, trust and safety, pricing summary, FAQ |
| `trainers.html` | Trainers and coaches: the tools it replaces, profile, booking, payments, programs, the between-sessions assistant, Communities, trainer pricing, founding offer |
| `gyms.html` | Gyms, studios, academies, and boxes: claiming a listing, affiliated trainers, the trainer-friendly program, classes, the Studio plan |
| `enthusiasts.html` | People who already train: specialist search, remote coaching, drop-ins while traveling, communities, rank and lineage, progress analytics |
| `get-started.html` | People starting out: matchmaking, prices up front, free consults, the first month, help between sessions |
| `pricing.html` | All plans, the Creator add-on, a full comparison table, pricing principles |
| `about.html` | The 2011 original, why the reboot runs the business, launch region, operator |
| `404.html` | Not-found page for GitHub Pages |

## Development

Plain static site: no build step, framework, analytics, or third-party scripts. Serve the folder and open it:

```bash
python3 -m http.server 14199 --bind 127.0.0.1
```

Then browse to http://127.0.0.1:14199.

- `styles.css`: styling with light and dark themes driven by CSS variables. Dark follows the system unless the visitor picks a theme with the toggle.
- `script.js`: theme toggle and mobile menu.
- `assets/`: the brand assets from the main Trainerdate repository (palette: Graphite `#202A29`, Forest `#456C52`, Leaf `#B9DF67`, Chalk `#F6F5EF`), plus web-sized derivatives: `logo-on-light.png`, `logo-on-dark.png`, `favicon.ico`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, and the Open Graph image `og-image.png`.
- `CNAME`, `robots.txt`, `sitemap.xml`.

Product illustrations (match cards, schedules, charts) are HTML and inline SVG, labeled as illustrations with example names. Replace them with real screenshots once the interfaces are approved.

## Calls to action

Trainerdate is in private alpha, so calls to action open an email to `hello@latticetech.ai` with a subject per audience (founding trainer, claim my gym, trainee early access). When the hosted app is live, point them at sign-up and add App Store and Google Play badges.

## Keeping it accurate

Product claims, plans, and prices come from the main repository's `TRAINERDATE_PLAN.md` (sections 5 to 10 and 13). Anything planned but not part of the founding beta carries a "Roadmap" tag. Update those tags and the pricing page as decisions change.

Writing follows `~/Code/Agents/requirements/WRITING_DOCUMENTS.md`: no em-dashes anywhere.

## Deployment

Pushing to `main` deploys through GitHub Pages (branch `main`, folder `/`). DNS for `trainerdate.com` must point at GitHub Pages: `A` records for `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, and `185.199.111.153`, and a `CNAME` for `www` to `jchristn.github.io`.

## Ownership

&copy; 2026 Lattice AI, LLC. All rights reserved. Like the Trainerdate platform, this site is not open source, and no license is granted.
