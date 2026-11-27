# Swagat Subhash Kalita

Hi, I'm Swagat, a backend-focused software engineer finishing my M.Sc. in Informatik (Computer Science). I care more about whether a claim about my code is actually true than whether it sounds impressive, which is why most of what's below comes with the test that proved it, not just a tech list.

Outside of code: I used to play competitive tennis in the BTV league, and used to work as a tennis instructor.

[Portfolio](https://swagatskalita092.github.io/) · [LinkedIn](https://linkedin.com/in/swagat-s-kalita) · [Email](mailto:swagatskalita2001@gmail.com)

---

## Selected work

### [ClearScan](https://clearscan.fyi): Software Engineer · [Engineering Dossier](https://github.com/swagatskalita092/clearscan-engineering)
A real, live resume-scoring and job-matching platform that I built and run solo, end to end. The free core isn't an AI wrapper. It's a deterministic scoring engine: TF-IDF over a 137-skill taxonomy, 62 O*NET job profiles, and a hand-tuned calibration curve. Anthropic only comes in for two paid features (bullet rewrites, cover letters), and that cost is covered by revenue. Built on FastAPI, React, and Supabase/PostgreSQL with row-level security, with Stripe Checkout handling payments through signed, idempotent webhooks. **1000+ scans · 238 tests · 500+ commits**

### [FlashBuy](https://github.com/swagatskalita092/flashbuy): Systems engineering project · [Engineering Journal](https://github.com/swagatskalita092/flashbuy/blob/main/python-service/docs/ENGINEERING_JOURNAL.md)
A flash-sale checkout backend built around one rule: stock can never be oversold, no matter how many buyers hit it at once. It uses row-level locking, idempotency keys, a Redis-backed waiting room with token-bucket admission, and leader election across replicas, the last piece hardened with a fencing token after someone pointed out a split-brain gap in an earlier version. I ran chaos drills by hand, killing the leader, Redis, and Postgres mid-sale: zero duplicate orders came out of it, though I've documented the one weak point honestly rather than hiding it (losing Redis also drops the in-flight queue state). A later piece adds a transactional outbox so a completely separate fulfillment service, with its own database and no shared transaction, learns of a confirmed order reliably over RabbitMQ. Chaos-testing that against the real containers found and fixed four real bugs along the way. **500/500 checkouts, zero oversold, p99 1.2s · 4 bugs found in outbox chaos tests**

### [Stack Overflow Developer Survey - Analytics Pipeline](https://github.com/swagatskalita092/Stack_Overflow_Pipeline): Data engineering project · [Live Dashboard](https://swagatskalita092.github.io/Stack_Overflow_Pipeline/site/) · [Engineering Journal](https://github.com/swagatskalita092/Stack_Overflow_Pipeline/blob/main/docs/engineering_journal.md)
Two real survey years (154,000+ responses) run through Airflow and dbt into a release/candidate/publish pattern with a per-year monotonicity guard, so a bad or partial run can never become the official answer. I proved that with six real failure injections against a live Postgres/Airflow stack. One of them, a truncated source file, actually got through before the fix existed. That's documented honestly in the engineering journal, along with a separate real bug the dashboard itself surfaced. **6 failure injections, zero corrupted publishes**

### [Fullproof Project Toolkit](https://github.com/swagatskalita092/fullproof-project-toolkit): Open-source methodology, skills & agent
This is the actual method behind the three projects above, written down so anyone can follow it: pick an idea, name the risks, build in verified phases, test adversarially, document honestly, bugs included. It comes as nine docs, a seven-domain idea bank, and two full idea-through-resume worked examples, all packaged as importable Claude skills. I also packaged the core methodology as a standalone Claude Code agent: it runs the whole pipeline on its own and hands back one verified report, dispatching a genuinely separate agent for its own second-opinion and verification steps instead of just checking its own work. **13 skills · 1 agent · 9 docs · DOI-archived on Zenodo**

---

## Core technologies

Python · FastAPI · PostgreSQL · Redis · RabbitMQ · React · TypeScript · Docker · GitHub Actions

---

<div align="center">

<a href="https://swagatskalita092.github.io/">Portfolio</a> · <a href="mailto:swagatskalita2001@gmail.com">Email</a> · <a href="https://linkedin.com/in/swagat-s-kalita">LinkedIn</a> · <a href="https://clearscan.fyi">ClearScan</a>
</div>
