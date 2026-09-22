# Intake events

Append only. Record the Linear event/comment identity, intake revision,
business-readable result, and immutable evidence reference for every processed
input, no-op, confirmation, and materialization handoff.

| Time | Event | Linear source | Revision | Result | Evidence |
| --- | --- | --- | ---: | --- | --- |
| 2026-09-22T15:15:21.352Z | knowledge.read | A8-135 7fb54a91-b04b-4167-8d92-35bc96a8cfb1 | 0 | Deterministic bounded read: INDEX plus two relevant documents | SOURCE-MANIFEST.md K-01..K-03 |
| 2026-09-22T15:16:01.644Z | target_question.created | comment 44115862-4f20-41e3-937a-9a2bea495d55 | 0 | Target question created and read back | comment 44115862-4f20-41e3-937a-9a2bea495d55 |
| 2026-09-22T15:16:02.656Z | milestone.recorded | comment a9c92c47-f2ba-461d-8705-4880161864a4 | 0 | Rolling intake milestone created and read back | comment a9c92c47-f2ba-461d-8705-4880161864a4 |
| 2026-09-22T15:46:08.809Z | target.spec_synced | comment c5c7d764-d624-484e-8b64-cc6a833da517 | 1 | Target NEW ，Anonymous Personal To-do v2`; Requirement Spec A8-137 verified | child a76d8d86-511d-4f2d-847f-726f9e119ac4 main Requirement Reviewing |
| 2026-09-22T15:46:44.720Z | clarification.requested | issue 7fb54a91-b04b-4167-8d92-35bc96a8cfb1 | 1 | First requirement confirmation requested and read back | comment 13bc8509-beae-4452-a0f2-561cfa66d17c |
| 2026-09-22T15:49:12.000Z | business.reply.matched | comment 0ec8d0dc-33c4-4981-befd-45d2a1c1ae1b | 1 | Newest unprocessed reply "confirmed" matched the pending revision-1 confirmation request | comment 0ec8d0dc-33c4-4981-befd-45d2a1c1ae1b |
| 2026-09-22T15:49:20.000Z | jev.human_confirmation | local gate human_confirmation revision 1 | 1 | JEV shadow: decision CONFIRMED confidence 0.77 (below min 0.90); wouldAction CONTINUE; deterministic match permits continuation | spec.md sha256 07c26e15d12e60d993c581096fd2c553772526bcfd67e750c7c77f902628beca |
| 2026-09-22T15:49:28.000Z | requirement.confirmed | comment 0ec8d0dc-33c4-4981-befd-45d2a1c1ae1b | 1 | Draft revision 1 frozen as spec.md (confirmed_revision 1) | spec.md sha256 07c26e15d12e60d993c581096fd2c553772526bcfd67e750c7c77f902628beca |
| 2026-09-23T00:00:00.000Z | WORKFLOW_SYNC_BLOCKED | local preflight | 1 | MATERIALIZATION_BLOCKED: filesystem write denied outside workspace root; GitHub network unreachable | exec mkdir C:\aiproject\anonymous-personal-to-do-v2 -> Access is denied; Test-NetConnection api.github.com:443 -> False |
| 2026-09-23T00:00:00.000Z | materialization.blocked | local preflight | 1 | Confirmed spec.md revision 1 preserved; repository/branch/worktree not created; no state change | spec.md sha256 07c26e15d12e60d993c581096fd2c553772526bcfd67e750c7c77f902628beca |
| 2026-09-23T00:10:00.000Z | WORKFLOW_SYNC_BLOCKED | Linear issue A8-135 | 1 | BLOCKER-3: Linear comment write unavailable; save_comment returned "MCP tool call requires approval, but approval policy is never" (2 attempts) | no linear comment id returned |
