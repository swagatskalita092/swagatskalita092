# Swagat Subhash Kalita

Backend-focused software engineer. Correctness first, then speed.

M.Sc. Informatik, Germany

[LinkedIn](https://linkedin.com/in/swagat-s-kalita) · [Email](mailto:swagatskalita2001@gmail.com)

---

## Selected work

### [ClearScan](https://clearscan.fyi): Software Engineer · [Engineering Dossier](https://github.com/swagatskalita092/clearscan-engineering)
Live resume-scoring and job-matching platform, built and run solo end to end. The free core is a deterministic, rule-based scoring engine (TF-IDF over a 137-skill taxonomy, 62 O*NET job profiles, a hand-tuned calibration curve) — not an AI wrapper; Anthropic is called only for two paid features (bullet rewrites, cover letters) where the cost is covered by revenue. FastAPI, React, Supabase/PostgreSQL with row-level security, Stripe Checkout with signed idempotent webhooks. **1000+ scans · 100+ users · 238 tests · 500+ commits**

### [FlashBuy](https://github.com/swagatskalita092/flashbuy): Systems engineering project · [Engineering Journal](https://github.com/swagatskalita092/flashbuy/blob/main/python-service/docs/ENGINEERING_JOURNAL.md)
A flash-sale checkout backend built to prove one invariant: fixed stock is never oversold, no matter how many buyers hit it at once. Row-level locking, idempotency keys, a Redis-backed waiting room with token-bucket admission, and multi-instance leader election hardened with a fencing token after outside feedback caught a split-brain gap. Hand-run chaos drills — killing the leader, Redis, and Postgres mid-sale — produced no duplicate orders, with one weak point documented rather than hidden (a Redis outage drops in-flight queue state). **500/500 checkouts, zero oversold, p99 1.2s**

### [Stack Overflow Developer Survey - Analytics Pipeline](https://github.com/swagatskalita092/Stack_Overflow_Pipeline): Data engineering project · [Live Dashboard](https://swagatskalita092.github.io/Stack_Overflow_Pipeline/site/) · [Engineering Journal](https://github.com/swagatskalita092/Stack_Overflow_Pipeline/blob/main/docs/engineering_journal.md)
Two real survey years (154,000+ responses) flow through Airflow and dbt into a release/candidate/publish pattern with a per-year monotonicity guard, so a bad or partial run can never become the official answer. Proven with six real failure injections against a live Postgres/Airflow stack — one (a truncated source file) genuinely got through before the fix existed, documented honestly in the engineering journal alongside a separate real bug the project's own dashboard surfaced. **6 failure injections, zero corrupted publishes**

### [Fullproof Project Toolkit](https://github.com/swagatskalita092/fullproof-project-toolkit): Open-source methodology, skills & agent
The phase-by-phase method behind the three projects above, written down so anyone can follow it: pick an idea, name the risks, build in verified phases, test adversarially, and document honestly including the bugs. Nine docs, a seven-domain idea bank, and two full idea-through-resume worked examples, packaged as importable Claude skills — plus a standalone Claude Code agent that runs the whole pipeline autonomously on a project and hands back one verified report, dispatching a genuinely separate agent for its own second-opinion and verification steps rather than checking its own work. **13 skills · 1 agent · 9 docs · DOI-archived on Zenodo**

---

## Also built

**[CRM Data Warehouse - Reporting Layer](https://github.com/swagatskalita092/Creating-reporting-layer-in-DWH-for-BI)**
A non-destructive PostgreSQL ETL pipeline (`CREATE TABLE IF NOT EXISTS`, truncate-and-reload, never a `DROP`) that cleans raw CRM tables into a `dwh` schema, deduplicating with a deterministic tie-break and logging data-quality issues without blocking the load. Feeds sales-performance, MRR, and customer lifetime-value views. **6 automated QA checks**

---

## Core technologies

Python · FastAPI · PostgreSQL · Redis · React · TypeScript · Docker · GitHub Actions

---

<div align="center">

<a href="mailto:swagatskalita2001@gmail.com">Email</a> · <a href="https://linkedin.com/in/swagat-s-kalita">LinkedIn</a> · <a href="https://clearscan.fyi">ClearScan</a>
</div>
