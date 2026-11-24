# Swagat Subhash Kalita

Backend-focused software engineer. Correctness first, then speed.

M.Sc. Informatik, Germany

[LinkedIn](https://linkedin.com/in/swagat-s-kalita) · [Email](mailto:swagatskalita2001@gmail.com)

---

## Selected work

### [ClearScan](https://clearscan.fyi): Software Engineer · [Engineering Dossier](https://github.com/swagatskalita092/clearscan-engineering)
Live resume-scoring and job-matching platform, built and run solo end to end. Deterministic scoring engine (TF-IDF + O*NET data, hand-tuned calibration), not an AI wrapper — Anthropic is used only for two paid features. FastAPI, React, Supabase/PostgreSQL with row-level security, Stripe. **1000+ scans · 87 users · 238 tests · 500+ commits**

### [FlashBuy](https://github.com/swagatskalita092/flashbuy): Systems engineering project · [Engineering Journal](https://github.com/swagatskalita092/flashbuy/blob/main/python-service/docs/ENGINEERING_JOURNAL.md)
Flash-sale checkout backend proven correct under real concurrent load: row-level locking, idempotency keys, a Redis waiting room, and leader election hardened with a fencing token after a bug was found in production-style testing. **500/500 checkouts, zero oversold, p99 1.2s**

### [Stack Overflow Developer Survey - Analytics Pipeline](https://github.com/swagatskalita092/Stack_Overflow_Pipeline): Data engineering project · [Live Dashboard](https://swagatskalita092.github.io/Stack_Overflow_Pipeline/site/) · [Engineering Journal](https://github.com/swagatskalita092/Stack_Overflow_Pipeline/blob/main/docs/engineering_journal.md)
Airflow + dbt pipeline over 154,000+ real survey responses, built around a candidate/publish pattern so a bad or partial run can never become the official answer. **6 real failure injections, zero corrupted publishes**

### [Fullproof Project Toolkit](https://github.com/swagatskalita092/fullproof-project-toolkit): Open-source methodology
The build → test adversarially → document method behind the three projects above, packaged as importable Claude skills so anyone can follow it. **13 skills · 9 docs · DOI-archived on Zenodo**

---

## Also built

**[CRM Data Warehouse - Reporting Layer](https://github.com/swagatskalita092/Creating-reporting-layer-in-DWH-for-BI)**
Non-destructive PostgreSQL ETL pipeline that cleans raw CRM data into BI-ready marts, with automated data-quality checks. **6 automated QA checks**

---

## Core technologies

Python · FastAPI · PostgreSQL · Redis · React · TypeScript · Docker · GitHub Actions

---

<div align="center">

<a href="mailto:swagatskalita2001@gmail.com">Email</a> · <a href="https://linkedin.com/in/swagat-s-kalita">LinkedIn</a> · <a href="https://clearscan.fyi">ClearScan</a>
</div>
