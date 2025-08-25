# [Taskcafe] business capabilities (TOGAF 10 L1–L3)

## Overview
- Repository: https://github.com/JordanKnott/taskcafe
- Primary language: TypeScript (frontend), Go (backend)
- Domain: Project and Work Management / Kanban boards

## L1–L3 capability map
- Level 1 Capability: Work Management
  - Level 2 Capability: Board Management
    - Level 3 Capability: Task groups (columns) & ordering
      - Evidence:
        - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/task.gql
        - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/task.resolvers.go
        - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/taskList.gql
  - Level 2 Capability: Task Lifecycle
    - Level 3 Capability: Create/Modify/Delete tasks
      - Evidence:
        - Mutations in schema: createTask, updateTaskName/Description, deleteTask
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/task.gql
        - Resolvers:
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/task.resolvers.go
    - Level 3 Capability: Update location/position (drag-drop)
      - Evidence:
        - Mutations: updateTaskLocation, sortTaskGroup
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/task.gql
    - Level 3 Capability: Status/Completion & Due date
      - Evidence:
        - setTaskComplete, updateTaskDueDate, due date notifications
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/task.gql
    - Level 3 Capability: Checklists & items
      - Evidence:
        - TaskChecklist & TaskChecklistItem models and mutations
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/task.gql
    - Level 3 Capability: Labels
      - Evidence:
        - add/remove/toggle task label
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/task.gql
    - Level 3 Capability: Comments & activity on tasks
      - Evidence:
        - create/update/deleteTaskComment, TaskActivity types
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/task.gql
  - Level 2 Capability: Task Querying & Lists
    - Level 3 Capability: My Tasks view & findTask
      - Evidence:
        - Query: myTasks (status/sort variants), findTask
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/schema.gql
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/task.gql

- Level 1 Capability: Collaboration
  - Level 2 Capability: Comments & Discussions
    - Level 3 Capability: Task comments (pinned, updates)
      - Evidence:
        - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/task.gql
        - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/task.resolvers.go
  - Level 2 Capability: Notifications
    - Level 3 Capability: Due-date notifications model
      - Evidence:
        - DueDateNotification, create/update/delete notification mutations
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/task.gql
    - Level 3 Capability: Notification domain
      - Evidence:
        - Notification schema/resolvers scaffold
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/notification.gql
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/notification.resolvers.go

- Level 1 Capability: Identity & Access Management
  - Level 2 Capability: Users, Teams & Roles
    - Level 3 Capability: Users & membership
      - Evidence:
        - Query: users, invitedUsers; Team/Project role mapping
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/schema.gql
        - Team/Project resolvers
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/team.resolvers.go
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/project.resolvers.go
    - Level 3 Capability: Role-based authorization
      - Evidence:
        - Directives: @hasRole(roles, level, type), @requiresUser
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/schema.gql

- Level 1 Capability: Analytics & Reporting
  - Level 2 Capability: Activity stream (per task)
    - Level 3 Capability: Activity types
      - Evidence:
        - ActivityType/TaskActivity types
          - https://github.com/JordanKnott/taskcafe/blob/master/internal/graph/schema/task.gql
  - Note: No dedicated analytics dashboards are evident; focus is on activity and “My Tasks” aggregations.

- Level 1 Capability: Integration & Extensibility
  - Level 2 Capability: GraphQL API
    - Level 3 Capability: End-to-end operations (projects, tasks, teams)
      - Evidence:
        - GraphQL schemas & resolvers
          - https://github.com/JordanKnott/taskcafe/tree/master/internal/graph/schema
          - https://github.com/JordanKnott/taskcafe/tree/master/internal/graph
  - Note: No plugin framework is visible; extensibility via API and frontend.

- Level 1 Capability: Platform & Operations
  - Level 2 Capability: Configuration & Migrations
    - Level 3 Capability: App config & schema migrations
      - Evidence:
        - https://github.com/JordanKnott/taskcafe/tree/master/conf
        - https://github.com/JordanKnott/taskcafe/tree/master/migrations
  - Level 2 Capability: Containerization
    - Level 3 Capability: Docker & Compose
      - Evidence:
        - https://github.com/JordanKnott/taskcafe/blob/master/Dockerfile
        - https://github.com/JordanKnott/taskcafe/blob/master/docker-compose.yml
        - https://github.com/JordanKnott/taskcafe/blob/master/docker-compose.dev.yml

## Capability map
```mermaid
flowchart TB
  subgraph WM[Work Management]
    B[Board management]
    B --> B1[Task groups (columns)]
    B --> B2[Sorting & location]
    C[Task lifecycle]
    C --> C1[Create/Modify/Delete]
    C --> C2[Move/Update location]
    C --> C3[Complete & Due date]
    C --> C4[Checklists]
    C --> C5[Labels]
    C --> C6[Comments & Activity]
    Q[Task querying]
    Q --> Q1[My Tasks]
    Q --> Q2[Find task]
  end
  subgraph COL[Collaboration]
    D1[Comments]
    D2[Notifications (Due date, domain)]
  end
  subgraph IAM[Identity & Access]
    E1[Users & Teams]
    E2[Role-based authorization]
  end
  subgraph AR[Analytics & Reporting]
    F1[Task-level activity stream]
  end
  subgraph INT[Integration & Extensibility]
    G1[GraphQL API]
  end
  subgraph OPS[Platform & Operations]
    H1[Config & Migrations]
    H2[Docker & Compose]
  end
```
