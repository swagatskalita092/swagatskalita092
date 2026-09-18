# Swagat Subhash Kalita

Backend-focused software engineer building and operating full-stack products.

M.Sc. Informatik, University of Passau · Germany
Open to Software Engineer / Backend / Full-Stack roles across Germany and the EU

[Portfolio](https://swagatskalita092.github.io) · [Résumé](https://swagatskalita092.github.io/resume.pdf) · [LinkedIn](https://linkedin.com/in/swagat-s-kalita) · [Email](mailto:swagatskalita2001@gmail.com)

---

## Selected work

### [ClearScan](https://clearscan.fyi): Founder & Engineer · [Engineering Dossier](https://github.com/swagatskalita092/clearscan-engineering)
Production résumé-scoring and job-matching platform, live since July 2026. 80+ registered users, 12 monthly paid subscribers, 900+ résumés parsed, under 6 seconds end-to-end. The free core scoring engine is deterministic and rule-based (TF-IDF, a custom skills taxonomy, O*NET occupational data, hand-tuned scoring with a calibration curve), not an AI wrapper. The Anthropic Claude API is limited to two paid features (bullet rewrites, cover letters) where the variable cost is justified by revenue. FastAPI, React, PostgreSQL/Supabase with row-level security, Stripe payments and webhooks, 29 API endpoints, 81 automated tests, 178 GitHub Actions deployments.

### [FlashBuy](https://github.com/swagatskalita092/flashbuy): Systems engineering project · [Engineering Journal](https://github.com/swagatskalita092/flashbuy/blob/main/python-service/docs/ENGINEERING_JOURNAL.md)
A flash-sale checkout backend built to prove correctness under real concurrent load: row-level locking, idempotency keys, a Redis-backed waiting room with token-bucket rate limiting, and multi-instance leader election. Load-tested with Locust at 500 concurrent users: 204 req/sec sustained, zero oversold units. Two real concurrency bugs were found and fixed during development (a connection-pool exhaustion issue and a false-failure race condition), and chaos testing (killing the database, cache, and app instances mid-load-test) confirmed zero duplicate orders and zero oversold inventory across every failure scenario, with one honestly documented weak point (in-flight queue state lost on a Redis outage).

### [Stack Overflow Developer Survey - Analytics Pipeline](https://github.com/swagatskalita092/Stack_Overflow_Pipeline): Data engineering project · [Live Dashboard](https://swagatskalita092.github.io/Stack_Overflow_Pipeline/site/) · [Engineering Journal](https://github.com/swagatskalita092/Stack_Overflow_Pipeline/blob/main/docs/engineering_journal.md)
Two real survey years (65,437 2024 responses, 89,184 2023 responses) flow through Airflow and dbt into a release/candidate/publish safety pattern with a per-year monotonicity guard, so a bad or partial run can never become the official answer. Proven with six real failure injections against a live Postgres/Airflow stack, killing the database mid-run and truncating a source file among them, with zero corrupted publishes. A real bug, an averages field silently NULL since the first version, was found only because the project's own dashboard forced a look at real per-cell coverage, one of several investigations the engineering journal documents start to finish. Salary USD conversion uses real historical ECB exchange rates and returns NULL, never a guess, for currencies it can't map, with one honestly documented weak point: Airflow's metadata database shares the warehouse Postgres instance, so killing it also stops the scheduler.

---

## Also built

**[CRM Data Warehouse - Reporting Layer](https://github.com/swagatskalita092/Creating-reporting-layer-in-DWH-for-BI)**
A non-destructive PostgreSQL ETL pipeline (`CREATE TABLE IF NOT EXISTS`, truncate-and-reload, `CREATE OR REPLACE VIEW`, never a `DROP`) that cleans raw CRM tables (`raw_customers`, `raw_subscriptions`, `raw_transactions`) into a `dwh` schema, deduplicating to one row per (sub_id, tx_date, status) with a deterministic tie-break (numeric from tx_id, then tx_id, then md5). Four data-quality issue types are logged in `dwh.dq_issues` (end date before start date, missing subscription, missing customer, transaction outside the subscription period) without blocking the load. Feeds `dwh.dm_sales_performance` plus monthly recurring revenue (annual amount / 12) and cumulative per-customer lifetime-value views, validated by 6 automated PASS/FAIL QA checks.

---

## Core technologies

Python · FastAPI · PostgreSQL · Redis · React · TypeScript · Docker · GitHub Actions

---

<div align="center">

<img src="https://github-stats-extended.vercel.app/api?username=swagatskalita092&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true" height="150"/>

</div>

---

<div align="center">

<a href="mailto:swagatskalita2001@gmail.com">Email</a> · <a href="https://linkedin.com/in/swagat-s-kalita">LinkedIn</a> · <a href="https://clearscan.fyi">ClearScan</a>
</div>
