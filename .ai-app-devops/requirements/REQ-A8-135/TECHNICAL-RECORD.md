# REQ-A8-135 technical record

## Status

Materialization checkpoint complete. No application code, migration, preview, or
deployment exists yet. The runtime contract below is fixed by the confirmed
requirement and the platform configuration; it is not yet implemented.

## Fixed technology contract (from the confirmed requirement and platform defaults)

- Next.js 16, React 19, TypeScript.
- Node.js Route Handlers with Zod validation at request boundaries.
- SQLite through Drizzle and `better-sqlite3`.
- `npm run db:migrate` reads `BUSINESS_DIRECT_SQLITE_PATH` and is rerunnable
  against the same database.
- `GET /api/health` returns HTTP 200 only after SQLite opens.
- Port pool `8081`-`8085`, bound host `0.0.0.0`; the application never chooses
  its own port.
- GitHub is source control only. No GitHub Actions deployment workflow.

## Identity

- Application: `anonymous-personal-to-do-v2`
- Requirement: `REQ-A8-135`
- Repository: https://github.com/air8uatrepo/anonymous-personal-to-do-v2 (public)
- Default branch: `master`
- Requirement branch: `req/REQ-A8-135`
- Worktree: `C:/aiproject/.worktrees/anonymous-personal-to-do-v2/REQ-A8-135`
- Runtime database path: `C:/aiproject/.local-app-data/anonymous-personal-to-do-v2/app.db`

## Confirmed baseline

`spec.md` revision 1, sha256
`07c26e15d12e60d993c581096fd2c553772526bcfd67e750c7c77f902628beca`.

## SDD artifacts

- `spec.md` confirmed business baseline (revision 1).
- `plan.md`, `tasks.md`, `testcases.md` are created in the developer phase and
  are never synced to Linear.

## Data safety

No secrets, database contents, logs, or real business data are recorded here.
The repository commits no `app.db`, `app.db-wal`, `app.db-shm`, log, or `.env`
file.
