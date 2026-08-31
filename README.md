## Falola Olufemi Adedeji

Full-stack engineer, five years. Most of what I've shipped lives in domains where
being wrong is expensive — escrow payments, school records, data purchases — so I
care disproportionately about the parts nobody demos: explicit transaction states,
honest error surfaces, and messages that tell a user where their money went.

Currently contracting with **RevStar Consulting**, and building the frontend for
**[Finaive](https://finaive.com)**, an AI-assisted escrow platform.

Based in Lagos — **the same working hours as Berlin, Paris, and Amsterdam**, and a
usable overlap with US Eastern.

### Worth reading

**[ledgerpay](https://github.com/falola13/ledgerpay)** · Go, PostgreSQL
A payments API built around a double-entry ledger. Idempotent charge retries keyed
on client tokens, a transactional outbox so no webhook is lost when the process dies
mid-write, HMAC-SHA256 signed delivery with retry and dead-letter handling, and
overdraft protection enforced by row-level locking. Five services under Docker
Compose, CI on every push. Not production card rails — a study of the correctness
patterns real payment systems depend on.

**[apihub-backend](https://github.com/falola13/apihub-backend)** · NestJS, Prisma, PostgreSQL
An API developer platform: hashed API keys, team management, usage analytics,
plan switching, and webhook delivery with retry. Pricing and retry rules live in
isolated policy classes so they can change without touching the delivery path.

**[TaskPulse-backend](https://github.com/falola13/TaskPulse-backend)** · NestJS, TypeORM, PostgreSQL
A productivity backend where the auth is the interesting part — HTTP-only JWT
cookies, Google and GitHub OAuth, and TOTP-based two-factor. Swagger docs at `/docs`.

There's a theme in those three I didn't plan: reliable delivery of events someone is
depending on, and the bookkeeping that proves it happened.

**[dispute-triage](https://github.com/falola13/dispute-triage)** · Python, Amazon Bedrock
The newest one, and the one pointed where I'm going. An LLM classifier for payment
disputes — and, the actual point, the evaluation harness that decides whether its
output is trustworthy: 90 hand-written labelled cases, per-class precision and recall
implemented by hand rather than imported, prompt versions scored against each other,
and a keyword baseline that runs in CI for free so the harness is exercised on every
push. The best prompt scores a perfect macro F1, which the README treats as a problem
rather than a headline — a benchmark everything passes has stopped measuring anything.

### What I'm learning

Moving into AI engineering, and working through the AWS generative AI certification.
The part I actually care about is evaluation — labelled sets, versioned prompts, and
regression tests that fail the build when quality drops, because that's what decides
whether model output is dependable enough to put in front of a user. dispute-triage
above is that argument made concrete instead of asserted: metrics hand-implemented so
the judgement calls stay visible, off-format answers counted as wrong rather than
quietly dropped, and the two failures that shaped the code written up in the repo
instead of tidied away. In progress, not finished. I'd rather show the work than
claim the title.

### Elsewhere

Portfolio · [falola.is-a.dev](https://falola.is-a.dev)
LinkedIn · [falola-olufemi](https://www.linkedin.com/in/falola-olufemi-87292625b)
Email · femi.deji0@gmail.com

