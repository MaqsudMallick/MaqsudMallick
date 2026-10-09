<h1 align="center">Maqsud Mallick</h1>

<p align="center">
  <b>Software Engineer</b><br>
  Backend systems, developer tooling, and the occasional thing<br>
  that has no business being written in C++.
</p>

<p align="center">
  <a href="mailto:maqsudmallick@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-maqsudmallick%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white"></a>
  <a href="https://linkedin.com/in/maqsud-mallick/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-maqsud--mallick-0A66C2?style=flat-square&logo=linkedin&logoColor=white"></a>
</p>

---

Two years' professional experience developing production SaaS applications, and a
knack for making the tool whenever there is no tool. TypeScript & Node, Java & Spring,
Python, some Go. Much of what I like to do ends up being around the data: consistency
guarantees, auth boundaries, query latencies.

Everything below is my own work and public. For employment history, see
[LinkedIn](https://linkedin.com/in/maqsud-mallick/).

---

## 🔗 Tendon — referential integrity for microservices

**[MaqsudMallick/tendon](https://github.com/MaqsudMallick/tendon)** · `Java 17` `Spring Boot` `PostgreSQL` `Prometheus`

The moment you divide your monolith, PostgreSQL will lose control of the constraints
it previously maintained automatically. `orders.customer_id` could refer to a customer
that no longer exists, and nothing will complain, since a foreign key cannot cross two
databases.

```text
orders.customer_id ──?──► customers.id    100 → 100 ✓   101 → 101 ✓   999 → ??? ✗ orphan
```

Tendon reconnects them. Aim it at your service databases using **read-only**
credentials, declare the cross-service relationships in a YAML contract, and it
constantly hunts for orphan references, reporting violations via REST and Prometheus.
No changes needed on your services.

The fascinating problem is that of false positives: the child row may well be validly
referring to a parent which has not yet been replicated. Thus, all candidates are
**aged and re-verified** before anything alerts, and the integrity SLOs allow one to
tolerate short in-flight references and still find lasting breakage. *Pre-alpha.*

## 🔬 Archon — autonomous deep-research agent

**[MaqsudMallick/deepresearch-agent](https://github.com/MaqsudMallick/deepresearch-agent)** · `Python` `LangGraph` `Qdrant` `SQLite`

An agent that does research on its own into a problem for an extended period of time.
**62 tools in 6 namespaces** (web, document, knowledge, synthesis, context, subagent)
using a LangGraph state machine with checkpointing to survive interruption and context
compression to survive its own length.

Forks out **subagents in isolation** to allow multiple research threads to run in
parallel. Each tool comes equipped with Pydantic-typed inputs and outputs, which is what
lets them chain without glue code. Includes the unsexy stuff, too — observability, retry
with backoff, rate limiting, and typed errors.

## Open source

**[Nextcloud](https://github.com/nextcloud)** — 5 merged PRs across the Mail app, Android client and Android library:

- [mail#13458](https://github.com/nextcloud/mail/pull/13458) — fixed an infinite recursion in the translation feature
- [android#17294](https://github.com/nextcloud/android/pull/17294) — scaled grid thumbnails to fill the available tile width
- [android#17251](https://github.com/nextcloud/android/pull/17251) — use clean internal links when the server reports `mod_rewrite` working
- [android-library#2079](https://github.com/nextcloud/android-library/pull/2079) — added the missing talk-password field in shares
- [android-library#2057](https://github.com/nextcloud/android-library/pull/2057) — added the core `mod-rewrite-working` capability

## Publication

**AI-Powered Medical Waste Management with IoT** — IEEE, March 2025. An IoT and deep
learning pipeline for real-time medical waste classification using ResNeXt, at 97.93%
accuracy.

## Also worth a look

| Project | What it is | Stack |
|---|---|---|
| **[kanban](https://github.com/MaqsudMallick/kanban)** · [live ↗](https://kanban-one-sable.vercel.app) | A kanban board over your *real* GitHub issues. Sign in, pick a repo, drag issues between columns — moves, labels, assignees, new issues and branch creation all write straight through to GitHub. | `Next.js` `TypeScript` `Octokit` |
| **[jpred](https://github.com/MaqsudMallick/jpred)** | Terminal UI time tracker built for job hunting. Three independent timers that auto-open the right tool for the task, goal alerts, session history, keyboard-first. | `Node 20` `TUI` |
| **[events-api](https://github.com/MaqsudMallick/events-api)** | Event registration REST API — JWT middleware, bcrypt hashing, Postgres, documented endpoints. Written to learn Go properly. | `Go` `PostgreSQL` |
| **[docmark-server](https://github.com/MaqsudMallick/docmark-server)** | Document annotation backend on Spring Security — JWT filter chain with custom entry-point and access-denied handling. | `Java` `Spring Boot` |
| **[ecommerce-scrapper](https://github.com/MaqsudMallick/ecommerce-scrapper)** · [live ↗](https://ecommerce-scrapper-six.vercel.app/) | Price comparison across Flipkart and Google Shopping, with Puppeteer and Cheerio scrapers behind a debounced search. | `Next.js` `Puppeteer` `Cheerio` |
| **[MinimalisticAssembler](https://github.com/MaqsudMallick/MinimalisticAssembler)** | A two-pass assembler and object loader for a toy instruction set, opcode table and all. | `C++` |
| **[GermanKeyboardDriver](https://github.com/MaqsudMallick/GermanKeyboardDriver)** | A custom Windows keyboard layout for typing German without a German keyboard. | `C++` |

## Stack

`TypeScript` `JavaScript` `Java` `Python` `Go` `C++` `SQL`
· `React` `Next.js` `Tailwind` `Redux` `TanStack`
· `Node.js` `NestJS` `Express` `Spring Boot` `TypeORM` `Mongoose` `LangGraph`
· `PostgreSQL` `MySQL` `MongoDB` `Redis` `Qdrant`
· `Docker` `GitHub Actions` `AWS` `Linux` `Prometheus` `Jest` `Zod` `OpenAPI`

## Education

**Jadavpur University** — BE Computer Science, 2020–2024. CGPA 8.98.

---

<p align="center">
  <sub><a href="mailto:maqsudmallick@gmail.com">maqsudmallick@gmail.com</a> ·
  <a href="https://linkedin.com/in/maqsud-mallick/">LinkedIn</a></sub>
</p>
