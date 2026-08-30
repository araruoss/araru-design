# Table pattern

Use for administrative information such as users, jobs, backups and logs. Define column priority, row actions, sorting, loading, empty, error and mobile list fallback. Never require horizontal scrolling for the primary action.

When the Server returns `{ items, pagination }`, keep pagination server-backed. Show the total when available, the current page, and explicit previous/next controls with disabled boundaries. Search and filters belong to the request contract and reset the page when changed. Preserve the current query while moving between pages.
