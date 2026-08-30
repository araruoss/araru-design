# Admin

Admin may be denser and use tables for Users, Jobs, Backups and Logs. Preserve Araru surfaces, status semantics and clear destructive confirmations. The merged Web client currently exposes General, Users, Roles and permissions, Libraries, Storage, Metadata, Jobs, Backup, Security and System destinations under the administrative context.

Admin navigation is a separate context: General, Appearance, Users, Profiles, Libraries, Storage, Metadata, Jobs, Backup, Security and System. Expanded layouts use an administrative sidebar; compact layouts use a navigation stack or drawer rather than compressing every destination into a narrow sidebar.

Settings use sections with title, description, fields and divider. Fields define default, changed, saving, saved, error, disabled, danger and restart-required states. Forms define inline validation, dirty state, submit, cancel, loading, success, error and unsaved-changes handling. General settings group instance identity, regional defaults and appearance; security settings group authentication/password policy, sessions, rate limits, cookies, reader policy and audit controls. Deployment-managed values remain read-only in the UI.

Users, Roles, Profiles, Jobs, Backups and Logs may use dense tables on expanded screens and compact lists on mobile. Each row has a stable accessible name and an action path that does not require horizontal scrolling. Searchable collections use server pagination with a visible result count, current page and previous/next controls; changing a search query returns to page one. Storage shows Local, Google Drive and Cloudflare R2 provider status, health, configure, test and disable actions; secrets are never rendered.

## Permission selector

Role forms present permissions grouped by product area rather than as one unstructured list. Each group has a translated area label, a selected-count indicator and a group-level checkbox that supports the indeterminate state. Individual permissions show a human-readable action and retain the technical `area.action` key as secondary context. System roles are protected and display their predefined access without exposing an editable selector.

## Administrative tabs

Use tabs only for sibling views at the same hierarchy. The active view is represented in the URL query state so it can be bookmarked and restored. Tabs must remain keyboard reachable, announce the active tab, and reflow to a scrollable or compact navigation treatment before content is clipped on narrow screens. Examples in the merged client include Jobs overview, executions, schedules and job types; Metadata summary, providers and processing; and Security authentication, sessions, rate limits, cookies, reader and audit views.

## Operational states

Administrative surfaces must define loading, empty, error, unauthorized, disabled, saving, saved and destructive-confirmation states. Job status pairs text with an icon or structural treatment and uses queued, running, completed, failed and cancelled values from the Server contract. Long-running actions such as library scans return an accepted/queued state and provide a path to Jobs rather than blocking the form.

## Implementation boundary

The Server contract is authoritative for permissions, persistence, validation and authorization. The Web guard improves navigation but must not be treated as security. Do not add providers, permissions, settings or destinations to this system unless they exist in the current Server and Web implementation; future capabilities must be labelled `planned`.
