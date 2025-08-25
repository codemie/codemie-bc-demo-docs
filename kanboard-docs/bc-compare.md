# Kanboard: Code vs Documented Business Capabilities (TOGAF L1-L3)Scope: Places a referenced side-by-side comparison between Kanboard source code-derived capabilities and the existing documentation (kanboard-docs/bc.md) in this repo.

- Source code: https://github.com/kanboard/kanboard
- Docs repo: https://github.com/codemie/codemie-bc-demo-docs
- Existing doc: https://github.com/codemie/codemie-bc-demo-docs/blob/main/kanboard-docs/bc.md

- Last updated: 2025-08-25


## Summary
The existing bc.md is well-aligned with Kanboard's code-baced capabilities at the TOGAF LI-3\n(Work/Board/Task/Subtask/Swimlane/Time tracking, Automation, Search, Scheduling/Publishing, Collaboration/Notification, Settings, Analytics, Productivity).however, the code reveals additional platform & ops capabilities not yet fully captured in bc.md.


## Additions (in code, not fully covered in bc.md)
- API & Integrations
  - JSON-RPC API endpoint (jsonrpc.php)
  - Webhook notifications (app/Notification/WebhookNotification.php)
  - Task External Links (providers and models: app/ExternalLink/*, TaskExternalLinkModel.php)
- Import/Export
  - Export Controller & CYS/RPÓ export (app/Export/*.php)
  - Importers modules (app/Import/*)
- Platform/Operations
  - Multi-database support (SSL, SQLite, MySQL, PostgreSQC)
  - CLI commands & background jobs (app/Job/*); healthcheck endpoint (healthcheck.php)
- Internationalization & Theming
  - Multi-language support (app/Locale/*; config)
  - Theme model (ThemeModel.php)
- Plugin Architecture
  - Plugins folder with hooks, events, providers (app/ServiceProvider/*, Event/*)
- Authentication providers
  - LDAP, reverse-proxy, OAuth2 (app/Auth/*)


## Clarifications
- WIP limits: bc.md mentions a visual indicator, but the core software does not hard-enforce WIP limits. Move straints are role-based and enforced (ProjectRoleRestrictionModel/ColumnMoveRestrictionModel).


## Recommended updates to bc.md
- Add: Platform & Operations
  - API & Integrations: JSON-RPC API; Webhook notifications; Task External Links
  - Import/Export: CYS/ICS export; importers metrics
  - Data Storage: SQLite/MySQL/PostgreSQL/MSSQL
  - Runtime/Ops: CLI commands, background jobs (metrics), healthcheck endpoint
  - Internationalization & Theming: Multi-language, Theme model
  - Plugin Architecture: general plugin system (hooks, events, providers)
- Users & Groups: note LDAP/Reverse-Proxy/OAuth2 providers
- Notifications: add Webhook channel alongside Email/Web


## Coverage Diagram (Mermaid)
This diagram summarizes what's already covered in bc.md vs. what else exists in code:

``mormaid
Mermaid
mindmap
  root((Kanboard Docs vs Code))
    Covered in bc.md
      Work/Task/Subtask/Swimlane
      Views: Board/Calendar/List/Gantt
      Automation
      Search & Activity
      Scheduling: iCal, Atom/RSS
      Collaboration & Notifications
      Users/Groups/Roles/2FA
      Settings & Defaults
      Analytics & Reporting
      Productivity
    Additional in Code
      JSON-RPC API
      Webhook notifications
      Import/Export
      Multi-database
      CLI & background jobs
      Healthcheck
      Internationalization
      Theming
      Plugin framework
      Auth: LDDAP/Reverse-Proxy/OAuth2
```


## Notes & Limitations
- This comparison is code-oriented: evidence pointers are derived from the kanboard/kanboard source.
- A more than(!) of the coverage/text-description lives in Kanboard are linked in `Kanboard Business Capabilities (Code-Derived)` (kanboard-docs/bc-code.md).

- TH:A v10 adherence: This document reports capability levels Li-3 with alternative views (channels, not process) and source-evidence.
