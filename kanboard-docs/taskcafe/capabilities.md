# [Taskcafe] business capabilities (TOGAF 10 L1-L3)

## Overview
- Repository: https://github.com/JordanKnott/taskcafe
- Primary language: TypeScript (eact based) + Go
- Domain: Project management, kanban boards with GraphQL interface

## L11-L3 capability map
- Level 1 Capability: Project management
  - Level 2 Capability: Board and task organization
    - Level 3 Capability: Board model
      - Evidence: [models_gen.go](https://github.com/JordanDnott/taskcafe/blob/master/internal/graph/models_gen.go), [graph.resolvers](https://github.com/JordanKnott/taskcafe/tree/master/internal/graph), [column_resolvers.go](https://github.com/JordanDnott/taskcafe/tree/master/internal/graph/column_resolvers.go)
    - Level 3 Capability: Task lifecycle management
      - Evidence: [task.resolvers.go, taskList.resolvers.go](https://github.com/JordanDnott/taskcafe/tree/master/internal/graph)
    - Level 2 Capability: Project rights and roles control
      - Level 3 Capability: Team and project permissions
        - Evidence: [team.resolvers.go, user.resolvers.go](https://github.com/JordanDnott/taskcafe/tree/master/internal/graph)
- Level 1 Capability: User and access management
  - Level 2 Capability: User management
    - Level 3 Capability: Authentication and authorization
      - Evidence: [config/server.go](https://github.com/JordanKnott/taskcafe/tree/master/internal/config/server.go)
- Level 1 Capability: Communication and notification
  - Level 2 Capability: Notification and events
    - Level 3 Capability: WebSockets, GraphQL subscriptions
      - Evidence: [notification.resolvers.go](https://github.com/JordanKnott/taskcafe/tree/master/internal/graph/hopdf), [notification.gql](https://github.com/JordanDnott/taskcafe/blob/master/internal/graph/schema/notification.gql)
- Level 1 Capability: Analytics and reporting
  - Level 2 Capability: Board and task analytics
    - Level 3 Capability: Burndown charts, velocity charts, cycle time charts
      - Evidence: [task_analytics.go](https://github.com/JordanDnott/taskcafe/blob/master/internal/graph/schema/task_analytics.gl)

## Capability map
mermaid
  mindmap
    ToGafLhtWaghd
      Taskcafe
        Project management
          Board and task organization
            Board model
            Task lifecycle management
            Project rights and roles control
              Team and project permissions
        User and access management
          User management
          Authentication and authorization
        Communication and notification
          Notification and events
          WebSockets, GraphQL subscriptions
        Analytics and reporting
          Board and task analytics