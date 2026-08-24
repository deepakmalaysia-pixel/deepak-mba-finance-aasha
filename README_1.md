# The Finance Floor — MBA Finance Skills Roadmap

An interactive, role-based skills roadmap for MBA Finance graduates entering the Indian job market. Built for [Aasha Infinite Foundation](https://github.com/) in the same spirit as the `new-age-skills` roadmap, adapted for the finance stream.

**Live structure:** one page (`index.html`), no build step, no dependencies beyond Google Fonts (loaded via CDN at runtime).

## What it covers

Six role-based tracks, each with a four-quarter path (Foundation → Tools & Certification → Domain Mastery → Placement Sprint):

| Ticker | Track | Core tools/areas |
|---|---|---|
| `EQTY` | Equity Research & Stock Broking | Equity, bonds, NISM, valuation, Excel |
| `MFWM` | Mutual Funds & Wealth Management | Mutual funds, bonds, AMFI/NISM, taxation of investments |
| `FDAT` | Financial Data Analytics | Advanced Excel, Power BI, SQL, statistics, FP&A |
| `ACTX` | Accounting, Taxation & Financial Reporting | Tally Prime, GST, Income Tax Act, Ind AS, audit |
| `FCAD` | Financial Consulting & Advisory | Corporate finance, valuation, case method, Excel |
| `CFRO` | Corporate Finance, Retail & ERP Operations | SAP FICO, Tally ERP9, working capital, Power BI |

Every track's badges and the top filter bar map to the requested skill areas: **advanced Excel, Tally/ERP9/SAP, Power BI, GST & taxation, equity/mutual funds/bonds, statistics & SQL** — click a filter chip to dim every track that doesn't touch that tool.

All resources cited are free or low-cost and publicly available: NISM/AMFI/ICAI/GST portal/Income Tax Department material, Tally's own courseware, Microsoft Learn, and well-known public YouTube channels. No paywalled or fabricated sources.

## Deploying to GitHub Pages

```bash
# from inside this folder
git init
git add .
git commit -m "Initial commit: MBA Finance skills roadmap"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Then in the repo on GitHub: **Settings → Pages → Source → Deploy from branch → `main` / `root`**. The site will be live at `https://<your-username>.github.io/<repo-name>/` within a couple of minutes.

## Editing content

Everything lives in `index.html` — no templating layer:

- Each track is a `<details class="track" data-tags="...">` block. Add a new track by copying an existing block and updating the ticker code, name, tagline, badges, demand label, roles line, and the four `.q` quarter blocks.
- `data-tags` on each `<details>` controls which filter chips affect it. Use any combination of: `excel`, `erp`, `powerbi`, `tax`, `markets`, `stats` — or add a new tag and a matching `<button class="chip" data-tag="...">` in the filter row.
- Colours, type, and spacing are all CSS custom properties at the top of the `<style>` block (`--gold`, `--gain`, `--ink`, etc.) if you want to re-theme it.

## Suggested next steps

- Link this roadmap to a student-facing intake form or WhatsApp group per track, the way Module 1 delivery was structured.
- Add a QR-code print version of each track's Q1 for students without laptops, following the same two-track delivery model used for Kalika Setu.
- Swap in AIF-specific mentor contacts or webinar dates under each quarter's resources once scheduled.
