# anonymous-personal-to-do-v2 - agent operating guide

This versioned file records the default Business Direct application stack and
the specification-driven rules for future changes. A confirmed requirement may
replace a default only when its SDD artifacts record that decision.

## Default technology stack

- Next.js 16, React 19, and TypeScript.
- Node.js through Next.js Route Handlers, with Zod validation at request
  boundaries.
- SQLite through Drizzle and `better-sqlite3`.
- GitHub for source control; no GitHub Actions deployment workflow is created.

## Local runtime contract

- Read SQLite only through the server. Its path comes from
  `BUSINESS_DIRECT_SQLITE_PATH`; do not commit the database file, WAL, shared
  memory file, logs, or `.env` values.
- Provide `npm run db:migrate`, which applies every local migration using
  `BUSINESS_DIRECT_SQLITE_PATH`.
- Provide `GET /api/health`. It returns HTTP 200 only after the application can
  open SQLite.
- The platform adapter starts the application with `npm run dev -- --hostname
  0.0.0.0 --port <allocated-port>`. Only ports `8081` through `8085` are
  available. Do not choose another port in application code.
- The runtime serves one development environment. Do not introduce Supabase,
  Vercel, GitHub Actions deployment, or separate test/staging/production
  configurations without an approved workflow change.

## Specification-driven development

Every change follows this order:

1. `brainstorming` for business clarification.
2. `writing-plans` for an approved implementation plan.
3. `test-driven-development` for Red-Green-Refactor.
4. `systematic-debugging` for a failing check.
5. `verification-before-completion` before any completion claim.

Per-requirement artifacts live in `specs/<requirement-id>/`:

- `spec.md` is the confirmed business baseline.
- `plan.md` is the approved implementation plan.
- `tasks.md` contains independently verifiable work.
- `testcases.md` contains acceptance-derived tests.

The workflow state lives in `.ai-app-devops/requirements/<requirement-id>/`.
`STATE.md` is authoritative for workflow state; `EVENTS.md` and `OUTBOX.md`
are append-only ledgers.

## Quality bar

Run the repository's own checks before claiming a change works:

- `npm test`
- `npm run lint`
- `npm run build`
- `npm run test:e2e`

## Managed file

<!-- BEGIN:air8-business-direct:agents -->
This file is created and managed by the Business Direct workflow
(`workflow_type: business_direct_app_v1`). `next dev` may append its own
managed Next.js agent-rules block; preserve both blocks.
<!-- END:air8-business-direct:agents -->
