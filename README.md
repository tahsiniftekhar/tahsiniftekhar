### Hi, I'm Tahsin Iftekhar

Backend-focused software engineer in Dhaka (GMT+6), 4+ years building SaaS and enterprise products in TypeScript, Node.js and PostgreSQL. Most of my work is on EU Digital Product Passport (ESPR) platforms, which trace products from raw materials to recycling.

I build systems where correctness matters: stock that can't be oversold, retries that don't double-charge, and concurrent edits that don't overwrite each other. Each project below comes with tests designed to fail if the guarantee breaks.

### Projects

**[Lynor](https://www.lynorco.com)**, an e-commerce platform I designed, built and run in production · [case study](https://tahsiniftekhar.com/work/lynor)
NestJS API behind two Next.js apps (storefront and staff dashboard). Orders take stock with a conditional update inside one transaction. SMS and email go through a transactional outbox instead of a job queue. 650+ API tests gate every release. Self-hosted with Docker and Caddy, with versioned rollbacks and hourly encrypted backups. The code is private.

**[Flowboard](https://github.com/tahsiniftekhar/flowboard)**, a shared Kanban board that stays correct under concurrent edits · [live](https://flowboard.tahsiniftekhar.com) · [case study](https://tahsiniftekhar.com/work/flowboard)
Card moves lock the parent row in id order. The race tests, including a stale move that must return 409, fail on a no-locks branch in CI.

**[Ping](https://github.com/tahsiniftekhar/ping)**, real-time chat on my own API · [live](https://ping.tahsiniftekhar.com) · [case study](https://tahsiniftekhar.com/work/ping)
I built the client against a third-party chat API first, then wrote a compatible Express, Socket.io and MongoDB backend. It has idempotent sends, per-conversation ordering and replay on reconnect.

**[Sneaker Drop](https://github.com/tahsiniftekhar/sneaker-drop)**, a lab for limited-stock reservations · [live](https://sneaker-drop.tahsiniftekhar.com) · [writeup](https://github.com/tahsiniftekhar/sneaker-drop/blob/develop/docs/reservations.md)
I benchmarked a conditional update against `SELECT … FOR UPDATE`; the conditional update was 15–35% faster at 8+ concurrent buyers. Expiry runs as a database sweeper. The tests catch all 8 past bugs when I reintroduce them.

### Stack

**Backend:** TypeScript, Node.js, NestJS, Express, Socket.io
**Data:** PostgreSQL, Prisma, Redis, MySQL, MongoDB
**Ops:** Docker, Caddy, GitHub Actions, AWS, Kubernetes, OpenTelemetry
**Frontend:** React, Next.js, TanStack Query

### Contact

[tahsiniftekhar.com](https://tahsiniftekhar.com) · [LinkedIn](https://linkedin.com/in/tahsiniftekhar) · dev.tahsiniftekhar@gmail.com · Open to remote roles overlapping UK/CET hours
