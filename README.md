# TaskForge 10/10 UI upgrade

Replace:
- client/src/App.jsx
- client/src/main.jsx
- client/src/styles.css

This version keeps the existing API contract and adds a real SaaS-style dashboard: overview/Kanban, filtered task queue, timeline, team/invite, settings, global search, notifications, task comments, create/edit/delete, project creation, Socket.IO refresh, responsive mobile UI, loading/empty/error states.

Your existing invite endpoint is used honestly: if it currently adds an existing account by email, the UI says so rather than pretending it sends email. For a production invite system, add a persistent invitation table with project_id, invited_email, role, token_hash, expires_at, accepted_at, invited_by and created_at, plus server-side RBAC.
