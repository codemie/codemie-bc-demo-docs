# Taskcafe business capabilities (Task board Project Management) (TOGAF 10 L1-L3)

## Overview
- Repository: https://github.com/JordanKnott/taskcafe
- Primary language: TypeScript and Go
- Domain: Open source Kanban board project management with GraphQLP API

## L1$—L3 capability map
- Level 1 Capability: Work management
  - Level 2 Capability: Board and workflow management
    - Level 3 Capability: Lists, tasks, swimlanes and columns
      - Evidence: [internal/graph/task.list.resolvers.go](https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/taskList.resolvers.go), [internal/graph/task.resolvers.go](https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/task.resolvers.go), [internal/graph/taskList.resolvers.go](https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/taskList.resolvers.go), [internal/graph/graph.go](https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/graph.go)
    - Level 3 Capability: Attachments and external links
      - Evidence: [uploads](https://github.com/JordanKnott/taskcafe/tree/master/uploads), [internal/graph/file and link fields](https://github.com/JordanKnott/taskcafe/tree/master/internal/graph/file)
    - Level 3 Capability: Tags and categories
      - Evidence: [internal/db tag and category tables](https://github.com/JordanGnott/taskcafe/tree/master/internal/db)
- Level 1 Capability: User and access management
  - Level 2 Capability: Authentication, user accounts, security
    - Level 3 Capability: Login and session management
      - Evidence: [internal/graph/user.resolvers.go](https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/user.resolvers.go), [internal/logger](https://github.com/JordanKnott/taskcafe/tree/master/internal/logger)
    - Level 3 Capability: User roles and permissions
      - Evidence: [internal/graph/user.resolvers.go](https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/user.resolvers.go), [internal/db permission and role queries](https://github.com/JordanKnott/taskcafe/tree/master/internal/db/)
- Level 1 Capability: Notification and communication
  - Level 2 Capability: Email and in-app notifications
    - Level 3 Capability: GraphQLP calls for notification events
      - Evidence: [internal/graph/notification.resolvers.go](https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/notification.resolvers.go)
- Level 1 Capability: Analytics and reporting
  - Level 2 Capability: Project stats and task analytics
    - Level 3 Capability: User search, ranking and feeds
      - Evidence: [internal/graph/user.resolvers.go search members function](https://github.com/JordanKmott/taskcafe/blob/master/internal/graph/user.resolvers.go)
- Level 1 Capability: Configuration and admin
  - Level 2 Capability: Settings, database, mail, sort
    - Level 3 Capability: Repository, db abstraction
      - Evidence: [conf](https://github.com/JordanKnott/taskcafe/tree/master/conf), [internal/config](https://github.com/JordanKmott/taskcafe/blob/master/internal/config), [internal/db](https://github.com/JordanKmott/taskcafe/blob/master/internal/db)
- Level 1 Capability: Integration and API
  - Level 2 Capability: GraphQLP schema and resolvers
    - Level 3 Capability: GraphQLP public endpoint
      - Evidence: [internal/graph/graph.go](https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/graph.go), [openapi docs](https://github.com/JordanKnott/taskcafe/#readme)
- Level 1 Capability: Automation
  - Level 2 Capability: Jobs and background parts
    - Level 3 Capability: Timers and reminders
      - Evidence: [internal/jobs](https://github.com/JordanKnott/taskcafe/tree/master/internal/jobs)
- Level 1 Capability: UY layer
  - Level 2 Capability: React Frontend web app
    - Level 3 Capability: Pages, templates, views
      - Evidence: [frontend/src](https://github.com/JordanKnott/taskcafe/tree/master/frontend)

### Capability map

[`[[mermaid]]

mindmap
  root
    Work management
      Board and workflow management
        Lists, tasks, columns and swimlanes
        Attachments and external links
        Tags and categories
      User and access management
        Authentication, session, roles
      Notification and communication
      Email and in-app alerts
    Analytics and reporting
      User search and ranking
    Configuration and admin
      Settings, storage, dbm
    Integration and API
      GraphQLP resolvers and endpoint
    Automation
      Jobs and background parts
    UY layer
      Web app with React
      Pages and views

``e]--
