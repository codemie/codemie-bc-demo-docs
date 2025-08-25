# [Kanboard] business capabilities (TOGAF 10 L1–L3)

## Overview
- Repository: https://github.com/kanboard/kanboard
- Primary language: PHP
- Domain: Project and Work Management / Kanban boards

## L1–L3 capability map
- Level 1 Capability: Work Management
  - Level 2 Capability: Board Management
    - Level 3 Capability: Columns & Swimlanes
      - Evidence: 
        - https://github.com/kanboard/kanboard/blob/main/app/Model/ColumnModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Model/SwimlaneModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/BoardViewController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/ColumnController.php
    - Level 3 Capability: Column move restrictions
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/ColumnMoveRestrictionModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/ColumnMoveRestrictionController.php
  - Level 2 Capability: Task Lifecycle
    - Level 3 Capability: Create/Modify tasks
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/TaskCreationModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Model/TaskModificationModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/TaskCreationController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/TaskModificationController.php
    - Level 3 Capability: Move/Reorder/Position
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/TaskPositionModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/TaskMovePositionController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/TaskReorderController.php
    - Level 3 Capability: Status/Recurrence
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/TaskStatusModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Model/TaskRecurrenceModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/TaskRecurrenceController.php
    - Level 3 Capability: Subtasks
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/SubtaskModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/SubtaskController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/SubtaskStatusController.php
    - Level 3 Capability: Tags & Categories
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/TagModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Model/CategoryModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/ProjectTagController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/CategoryController.php
    - Level 3 Capability: Files & External links
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/FileModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Model/TaskFileModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Model/TaskExternalLinkModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/FileViewerController.php
  - Level 2 Capability: Search & Filter
    - Level 3 Capability: Custom filters & advanced search
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/CustomFilterModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Model/TaskFinderModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/SearchController.php

- Level 1 Capability: Collaboration
  - Level 2 Capability: Comments & Discussions
    - Level 3 Capability: Comments (list/mail)
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/CommentController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/CommentListController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/CommentMailController.php
  - Level 2 Capability: Notifications & Feeds
    - Level 3 Capability: User/Project notifications
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/UserNotificationModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectNotificationModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/WebNotificationController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Core/Mail
    - Level 3 Capability: Feeds (calendar/RSS)
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/ICalendarController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/FeedController.php

- Level 1 Capability: Identity & Access Management
  - Level 2 Capability: Users & Groups
    - Level 3 Capability: User & group management
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/UserModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Model/GroupModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/UserModificationController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/GroupListController.php
  - Level 2 Capability: Roles & Permissions
    - Level 3 Capability: Project permissions/roles
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectPermissionModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectRoleModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/ProjectPermissionController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/ProjectRoleController.php
  - Level 2 Capability: Auth & MFA
    - Level 3 Capability: OAuth & Two-Factor
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/OAuthController.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/TwoFactorController.php
        - https://github.com/kanboard/kanboard/tree/main/app/Core/Ldap

- Level 1 Capability: Analytics & Reporting
  - Level 2 Capability: Project stats & analytics
    - Level 3 Capability: Daily/column stats, task analytics
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectDailyColumnStatsModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Model/TaskAnalyticModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/AnalyticController.php
  - Level 2 Capability: Activity stream
    - Level 3 Capability: Project/Task activity
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectActivityModel.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/ActivityController.php
  - Level 2 Capability: Export
    - Level 3 Capability: CSV export
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/app/Core/Csv.php
        - https://github.com/kanboard/kanboard/blob/main/app/Controller/ExportController.php

- Level 1 Capability: Integration & Extensibility
  - Level 2 Capability: APIs & Plugins
    - Level 3 Capability: JSON-RPC API
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/jsonrpc.php
        - https://github.com/kanboard/kanboard/tree/main/app/Api
    - Level 3 Capability: Plugin architecture & hooks
      - Evidence:
        - https://github.com/kanboard/kanboard/tree/main/app/Core/Plugin
        - https://github.com/kanboard/kanboard/tree/main/app/ServiceProvider
    - Level 3 Capability: External links
      - Evidence:
        - https://github.com/kanboard/kanboard/tree/main/app/Core/ExternalLink

- Level 1 Capability: Platform & Operations
  - Level 2 Capability: Healthcheck & Monitoring
    - Level 3 Capability: Application healthcheck
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/healthcheck.php
  - Level 2 Capability: Config & Environment
    - Level 3 Capability: App config/environment
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/config.default.php
        - https://github.com/kanboard/kanboard/blob/main/Dockerfile
  - Level 2 Capability: Containerization
    - Level 3 Capability: Docker images & compose
      - Evidence:
        - https://github.com/kanboard/kanboard/blob/main/docker-compose.sqlite.yml
        - https://github.com/kanboard/kanboard/blob/main/docker-compose.mysql.yml
        - https://github.com/kanboard/kanboard/blob/main/docker-compose.postgres.yml

## Capability map
```mermaid
flowchart TB
  subgraph WM[Work Management]
    B[Board management]
    B --> B1[Columns & Swimlanes]
    B --> B2[Move restrictions]
    C[Task lifecycle]
    C --> C1[Create/Modify]
    C --> C2[Move/Reorder/Position]
    C --> C3[Status/Recurrence]
    C --> C4[Subtasks]
    C --> C5[Tags & Categories]
    C --> C6[Files & External links]
    S[Search & filter]
    S --> S1[Custom filters]
    S --> S2[Advanced finder]
  end
  subgraph COL[Collaboration]
    D1[Comments]
    D2[Notifications]
    D3[Feeds (Calendar/RSS)]
  end
  subgraph IAM[Identity & Access]
    E1[Users & Groups]
    E2[Roles & Permissions]
    E3[OAuth & 2FA]
  end
  subgraph AR[Analytics & Reporting]
    F1[Project stats & analytics]
    F2[Activity stream]
    F3[Export (CSV)]
  end
  subgraph INT[Integration & Extensibility]
    G1[JSON-RPC API]
    G2[Plugins & hooks]
    G3[External link providers]
  end
  subgraph OPS[Platform & Operations]
    H1[Healthcheck]
    H2[Config & Env]
    H3[Docker & Compose]
  end
```
