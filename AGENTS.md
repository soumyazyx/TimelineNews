# Agent instructions: TimelineNews public policy

These are the canonical instructions for interactive repository maintenance.
Unattended model jobs follow their task prompts and enforced tool restrictions;
the coding-session checklist below is not part of their task.

## Reading order

1. At the start of a new conversation with the owner, call `memory_session_start`
   before answering and read its complete reply. Open with its status line and
   follow the returned standing rules. Do not repeat it merely because you change repos.
   If unavailable, open with "PMC unavailable: running without your standing rules"
   and say the owner's standing rules are not loaded.
2. Read this guide. Read root `HANDOVER.md` if active work later adds one.
3. Read the project documents listed below, then
   task-specific references and relevant decisions. Read recent journal entries
   when needed; do not load an entire historical journal by default.
4. Check the current branch and working tree before editing. Preserve existing
   changes. Resolve conflicting or stale claims from current rules, code and live
   evidence rather than assuming an old handover or log is still accurate.

## Repository boundaries

- Public policy repository containing [PRIVACYPOLICY.md](PRIVACYPOLICY.md), not the
  backend or mobile application. [README.md](README.md) is the project entry point;
  no application setup is required here.
- Keep public policy text consistent with actual product behavior and preserve
  externally referenced filenames/anchors. Do not invent effective dates or claims.
- Do not copy private notes, credentials, account identifiers or server details
  into public policy documents. Check changed Markdown/links; no app test runner exists.
- Remotes use SSH. The checkout still uses legacy `main`; the owner's branch
  convention is `master`. Renaming branches is outside this documentation pass.

## Documentation and completion

- Add root `HANDOVER.md` when there is active work to hand over. Keep
  it focused on current work; about 100 lines is a target, not a hard limit.
- A session that **creates a commit or materially changes behavior** must add a
  dated entry to `docs/WORKLOG.md`: what changed, why, verification and unresolved limits.
  Create the journal if that trigger occurs and it does not yet exist. Read-only
  investigation does not require an entry. Preserve dated history; add new entries first.
- Record consequential decisions in `docs/decisions/`. Existing historical decision
  records stay where documented until explicitly consolidated; do not rewrite their dates.
- Reconcile affected docs and check changed local links before wrapping up or deploying.
  Run checks appropriate to the change; Markdown-only edits do not require an app restart.
- PMC **Todos** are agent follow-ups and parked work. PMC **Tasks** are action
  reminders such as bills and renewals, including the owner's Tasks widget. Keep
  these separate. Repo-tag policy remains open; do not invent a fixed vocabulary,
  mass-retag memories or migrate an existing local backlog as part of a docs edit.
- Never add Co-Authored-By, generated-by or other AI attribution to commits or PRs.
