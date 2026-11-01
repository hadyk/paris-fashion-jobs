# Jobs that fit Hoda Kamel — wholesale & merchandising

A hand-curated snapshot of **55 live fashion wholesale, merchandising and business-development roles** matched against Hoda Kamel's CV (8 years in wholesale across Europe, the UK, the US and the GCC; collection merchandising, OTB, sell-through; 6 languages; Paris-based) — **30 in Paris**, 14 in London, 4 in the rest of Europe, 7 in New York.

Every entry was **verified live on 1 November 2026** and links straight to the original listing. Each card carries a fit score (0–5), "why it fits" bullets tied to the CV, and honest caveats. 13 roles are rated Exceptional (≥ 4.5).

**Live page:** https://hadyk.github.io/paris-fashion-jobs/

## Where the jobs came from

- [BoF Careers](https://www.businessoffashion.com/careers/) — wholesale (177), merchandising (115) and sales (714) feeds via RSS; details parsed from each job page (JSON-LD + data layer)
- [LinkedIn](https://www.linkedin.com/jobs/) — guest search API across 12 keyword × location combinations (~220 postings parsed), details from each job page
- [Kering careers](https://www.kering.com/en/talent/job-offers/) — Pomellato Wholesale Area Manager, Paris
- [ANINE BING (Greenhouse)](https://job-boards.greenhouse.io/aninebing) — Wholesale Manager EU & ME, Wholesale Director EMEA & APAC interim, both Paris
- [Welcome to the Jungle](https://www.welcometothejungle.com/) — Fusalp Senior Account Executive, CABAIA Sales Merchandiser
- [AMI Paris (Recruitee)](https://amiparis.recruitee.com/) — Wholesale Area Manager, the Americas
- [FashionUnited](https://fashionunited.fr/fashion-jobs) — SOEUR Wholesale Manager CDD, PVH Senior Wholesale Planner
- Probed but not fruitful this pass: Workday APIs (Chanel/Tapestry/Kering — confirmed no new Paris wholesale), Greenhouse boards (Reformation/Everlane — US retail), Lever, FashionJobs.com, WTTJ search (login-gated)

## The site

`site/` is a dependency-free static page: `index.html` + `data.js`. Features:

- Search, filter by location / function / contract / minimum fit, salary-known toggle
- Sort by best match, closing date, recency or salary
- Per-job fit score with CV-tied justification and caveats in the detail view
- Urgent-deadline bar and a three-step action plan
- Share button (system share sheet / copy link)

## Refresh the listings

Edit `site/data.js` (each job is one object) — new roles slot in automatically; stats, filters and sorting recompute client-side.

## Publish (already done once)

```bash
cd ~/paris-fashion-jobs
git init && git add -A && git commit -m "Jobs snapshot"
gh repo create paris-fashion-jobs --public --source=. --push
gh api repos/:owner/paris-fashion-jobs/pages -X POST -f build_type=workflow
```

> Listings expire without notice. Always confirm on the original ad before applying.
