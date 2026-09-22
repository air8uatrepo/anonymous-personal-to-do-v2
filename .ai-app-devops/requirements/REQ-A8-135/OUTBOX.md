# REQ-A8-135 outbox

Append only delivery ledger. An outbound item is re-sent only after its
recorded readback is missing or stale. Unverified items must not advance local
state.

| Idempotency key | Target | Kind | Revision | Status | Readback ID |
| --- | --- | --- | ---: | --- | --- |
| bd-intake-knowledge-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r1 | Local intake A8-135 | knowledge_cache | 1 | verified | SOURCE-MANIFEST.md |
| bd-intake-reply-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r0 | Linear issue 7fb54a91-b04b-4167-8d92-35bc96a8cfb1 | reply_request | 0 | verified | 44115862-4f20-41e3-937a-9a2bea495d55 |
| bd-intake-milestone-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r0 | Linear issue 7fb54a91-b04b-4167-8d92-35bc96a8cfb1 | rolling_milestone | 0 | verified | a9c92c47-f2ba-461d-8705-4880161864a4 |
| bd-intake-spec-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r1 | Linear child a76d8d86-511d-4f2d-847f-726f9e119ac4 | requirement_spec | 1 | verified | a76d8d86-511d-4f2d-847f-726f9e119ac4 |
| bd-intake-clarification-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r1 | Linear issue 7fb54a91-b04b-4167-8d92-35bc96a8cfb1 | requirement_clarification | 1 | verified | 13bc8509-beae-4452-a0f2-561cfa66d17c |
| bd-intake-confirmation-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r1 | Linear issue 7fb54a91-b04b-4167-8d92-35bc96a8cfb1 | confirmation_intake | 1 | verified | comment 0ec8d0dc-33c4-4981-befd-45d2a1c1ae1b |
| bd-intake-spec-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r2 | Linear child a76d8d86-511d-4f2d-847f-726f9e119ac4 | confirmed_spec_sync | 1 | verified | child a76d8d86-511d-4f2d-847f-726f9e119ac4 Requirement Done |
| bd-materialize-repo-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r1 | GitHub air8uatrepo/anonymous-personal-to-do-v2 | repository_creation | 1 | verified | https://github.com/air8uatrepo/anonymous-personal-to-do-v2 (public, default branch master) |
| bd-materialize-app-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r1 | C:/aiproject/anonymous-personal-to-do-v2 | application_directory | 1 | verified | canonical checkout at scaffold commit 7391546 |
| bd-materialize-worktree-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r1 | C:/aiproject/.worktrees/anonymous-personal-to-do-v2/REQ-A8-135 | worktree_creation | 1 | verified | git worktree list -> req/REQ-A8-135 at 7391546 |
| bd-materialize-spec-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r1 | worktree REQ-A8-135 | spec_freeze | 1 | verified | spec.md sha256 07c26e15d12e60d993c581096fd2c553772526bcfd67e750c7c77f902628beca |
| bd-materialize-agents-7fb54a91-b04b-4167-8d92-35bc96a8cfb1-r1 | worktree REQ-A8-135 | agent_guide | 1 | verified | commit 7391546 AGENTS.md marker air8-business-direct:agents |
