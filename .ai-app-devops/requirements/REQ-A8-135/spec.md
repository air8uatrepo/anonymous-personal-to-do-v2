# Requirement specification

Revision: 1 (business-confirmed)

## Application target

Anonymous Personal To-do v2 (new application; project_mode NEW)

## Goal

Provide an anonymous personal To-do application, version 2, that any visitor can
use immediately to manage their own tasks without registration or login.

## In scope

- Create a task by entering task text, with no account required.
- View the list of the visitor's own tasks.
- Mark an open task as completed.
- Restore a completed task back to open.
- Delete a task so it no longer appears in the list.
- Anonymous use throughout: no registration and no login at any point.
- Local runtime: SQLite persistence and a local Node.js preview host, with a
  health endpoint that reports ready only after the database opens.

## Out of scope

- User accounts, sign-up, sign-in, or any identity or profile management.
- Sharing tasks between people, teams, or devices.
- Notifications, reminders, scheduling, or due-date behavior.
- Cloud hosting, cloud deployment, or any cloud database.
- Any v2 behavior beyond the confirmed items listed above.

## Acceptance criteria

- AC-1: A visitor with no account can add a task by entering text, and the new
  task then appears in that visitor's list.
- AC-2: A visitor can view the list of their own tasks.
- AC-3: A visitor can complete an open task, and that task then shows as
  completed.
- AC-4: A visitor can restore a completed task, and that task then shows as
  open again.
- AC-5: A visitor can delete a task, and that task no longer appears in the
  list.
- AC-6: Completing, restoring, and deleting a task keep the other tasks
  unchanged.
- AC-7: No step in the flow requires registration or login.
- AC-8: The application is reachable at the local preview address and its
  health endpoint returns success only after the local database is available.

## Business examples

- EX-N-001: A first-time visitor opens the application, enters "DEMO-task-1" as
  a task, and immediately sees "DEMO-task-1" listed as open.
- EX-N-002: A visitor has an open task, marks it complete, and the task now
  appears as completed while all other tasks stay unchanged.
- EX-N-003: A visitor has a completed task, restores it, and the task appears
  as open again while all other tasks stay unchanged.
- EX-N-004: A visitor deletes a task, and that task is gone from the list while
  all other tasks stay unchanged.
- EX-E-001: A visitor submits empty task text, and no task is created.

## Assumptions and unresolved items

- Confirmed by the business owner on 2026-09-22: the baseline above is the
  accepted contract for this revision.
- UNRESOLVED: which additional behaviours, if any, distinguish v2 from the
  earlier anonymous personal To-do list. The business owner confirmed this
  baseline as sufficient to proceed; any later v2-specific behaviour is a new
  business decision and returns to business review.
- UNRESOLVED: no task text length or duplicate-task rule was stated; the
  confirmed baseline treats each added task as its own item.

## This change does not

- Introduce registration, login, or any account concept.
- Introduce sharing, collaboration, or multi-device sync.
- Introduce cloud deployment or a cloud database.
- Define any v2-specific behaviour that the business owner has not confirmed.
