# Kanboard Business Capability Model (TOGAF 10 aligned)

This document captures the business capabilities implemented by Kanboard, aligned to TOGAF 10 Business Architecture practices. It provides an L1–L3 capability map, brief descriptions, and source mappings to the codebase for traceability.

## Overview
Kanboard is a Kanban-centric project and task management application. Its capabilities span project/board management, task execution, user access and collaboration, analytics, configuration, and integrations.

## Capability Map
```mermaid
graph TD
  A[Kanboard Capabilities] --> B[Project Portfolio & Board Mgmt]
  A --> C[Task Management]
  A --> D[User & Access Mgmt]
  A --> E[Collaboration & Communication]
  A --> F[Analytics & Reporting]
  A --> G[Configuration & Administration]
  A --> H[Integration & Extensibility]
  A --> I[Scheduling & Calendar]
  A --> J[File & Document Mgmt]
  A --> K[Search & Filtering]

  subgraph B1[Project Portfolio & Board Mgmt]
    B --> B2[Boards]
    B --> B3[Columns]
    B --> B4[Swimlanes]
    B --> B5[Project Roles & Permissions]
    B --> B6[Tags & Categories]
    B --> B7[Project Files]
    B --> B8[Project Duplication]
  end

  subgraph C1[Task Management]
    C --> C2[Task CRUD]
    C --> C3[Subtasks]
    C --> C4[Comments]
    C --> C5[Attachments]
    C --> C6[Links (Internal/External)]
    C --> C7[Priority & Recurrence]
    C --> C8[Move/Reorder/Position]
    C --> C9[Bulk Ops]
    C --> C10[Import/Export]
    C --> C11[Status & Transitions]
    C --> C12[Templates]
  end

  subgraph D1[User & Access Mgmt]
    D --> D2[Authentication (2FA/OAuth/Reset)]
    D --> D3[Users (CRUD/Status/Locking)]
    D --> D4[Groups & Membership]
    D --> D5[Project Roles & Permissions]
    D --> D6[API Access]
    D --> D7[Captcha]
  end

  subgraph E1[Collaboration]
    E --> E2[Comments]
    E --> E3[Notifications (Web/Email)]
    E --> E4[Feeds & iCal]
    E --> E5[Activity Streams]
  end

  subgraph F1[Analytics & Reporting]
    F --> F2[Project Analytics (Daily/Columns/Transitions)]
    F --> F3[Task Analytics]
    F --> F4[Exports]
  end

  subgraph G1[Configuration]
    G --> G2[Settings]
    G --> G3[Locale/Timezone/Currency]
    G --> G4[Themes]
    G --> G5[Plugins]
    G --> G6[Security & Healthcheck]
    G --> G7[Cronjobs]
  end

  subgraph H1[Integration]
    H --> H2[JSON-RPC API]
    H --> H3[Events/Hooks]
    H --> H4[External Links]
    H --> H5[CLI]
  end

  subgraph I1[Scheduling & Calendar]
    I --> I2[iCalendar Feeds]
  end

  subgraph J1[File & Document]
    J --> J2[Avatars]
    J --> J3[Project Files]
    J --> J4[Task Files]
    J --> J5[File Viewer]
  end

  subgraph K1[Search & Filtering]
    K --> K2[Search]
    K --> K3[Custom Filters]
  end
```

## Capability Hierarchy L1–L3 with brief descriptions and source mappings

- L1 Project Portfolio & Board Management
  - L2 Board Design & Configuration
    - L3 Columns: Define and manage workflow stages
      - Source: app/Model/ColumnModel.php; app/Controller/ColumnController.php; ColumnRestriction/MoveRestriction
    - L3 Swimlanes: Parallel work streams per board
      - Source: app/Model/SwimlaneModel.php; app/Controller/SwimlaneController.php
    - L3 Tags & Categories: Classify work
      - Source: app/Model/TagModel.php, TaskTagModel.php; app/Controller/TagController.php; CategoryModel/Controller
  - L2 Project Governance
    - L3 Project Roles & Permissions: Control access
      - Source: ProjectRoleModel.php, ProjectPermissionModel.php, ProjectGroupRoleModel.php, ProjectUserRoleModel.php; Controllers
    - L3 Project Files: Attachments at project level
      - Source: ProjectFileModel.php; ProjectFileController.php
    - L3 Project Duplication/Templates: Reuse configurations
      - Source: ProjectDuplicationModel.php; ProjectActionDuplicationController.php

- L1 Task Management
  - L2 Task Lifecycle
    - L3 Task CRUD: Create, read, update, delete tasks
      - Source: TaskCreation/Modification/Status Controllers; TaskModel.php
    - L3 Status & Transitions: Move across columns and track transitions
      - Source: TaskStatusModel.php, TransitionModel.php; TaskMovePosition/TaskReorder controllers
    - L3 Positioning: Order within columns/swimlanes
      - Source: TaskPositionModel.php; BoardAjaxController.php
    - L3 Recurrence: Repeating tasks
      - Source: TaskRecurrenceModel.php; TaskRecurrenceController.php
    - L3 Bulk Operations: Bulk edit/move
      - Source: TaskBulk*.php controllers
    - L3 Templates/Predefined Content
      - Source: PredefinedTaskDescriptionModel.php; PredefinedTaskDescriptionController.php
  - L2 Task Decomposition & Collaboration
    - L3 Subtasks & Time Tracking
      - Source: SubtaskModel.php, SubtaskTimeTrackingModel.php; SubtaskController.php
    - L3 Comments & Mentions (basic comments)
      - Source: CommentModel.php; CommentController.php; CommentList/Mail controllers
    - L3 Links & Dependencies: Internal graph and external references
      - Source: TaskLinkModel.php, LinkModel.php; TaskInternalLinkController.php; TaskExternalLinkModel.php/Controller.php
    - L3 Files & Attachments
      - Source: TaskFileModel.php; TaskFileController.php; FileViewerController.php
    - L3 Import/Export
      - Source: Import/*; ExportController.php; Csv exporters in app/Export

- L1 User & Access Management
  - L2 Identity & Authentication
    - L3 Local Authentication & Password Reset
      - Source: AuthController.php; PasswordResetModel/Controller
    - L3 Two-Factor Authentication
      - Source: TwoFactorController.php
    - L3 OAuth
      - Source: OAuthController.php
    - L3 Captcha (bot mitigation)
      - Source: CaptchaModel.php; CaptchaController.php
    - L3 Remember-Me Sessions
      - Source: RememberMeSessionModel.php
  - L2 Account & Directory
    - L3 Users (CRUD, status/locking, last login)
      - Source: UserModel.php, UserLockingModel.php, LastLoginModel.php; User* controllers
    - L3 Groups & Membership
      - Source: GroupModel.php, GroupMemberModel.php; Group* controllers
    - L3 API Access Tokens
      - Source: UserApiAccessController.php; JSON-RPC endpoint (jsonrpc.php)

- L1 Collaboration & Communication
  - L2 Notifications & Feeds
    - L3 Web Notifications & Unread Queue
      - Source: WebNotificationController.php; UserUnreadNotificationModel.php
    - L3 Email Notifications
      - Source: NotificationModel.php, NotificationTypeModel.php; ProjectNotification* models
    - L3 RSS/Atom Feeds; iCalendar
      - Source: FeedController.php; ICalendarController.php
  - L2 Activity Streams
    - L3 Project Activity Log
      - Source: ProjectActivityModel.php; ActivityController.php

- L1 Analytics & Reporting
  - L2 Project Analytics
    - L3 Daily Stats; Column Stats; Transitions
      - Source: ProjectDailyStatsModel.php, ProjectDailyColumnStatsModel.php, TransitionModel.php; AnalyticController.php; app/Analytic
  - L2 Task Analytics
    - L3 Work Item Metrics
      - Source: TaskAnalyticModel.php; AnalyticController.php
  - L2 Exporting & Data Access
    - L3 CSV/JSON exports
      - Source: ExportController.php; app/Export

- L1 Configuration & Administration
  - L2 System Settings & Localization
    - L3 Settings
      - Source: SettingModel.php; ConfigController.php
    - L3 Languages/Locale; Timezone; Currency
      - Source: LanguageModel.php; app/Locale/*; TimezoneModel.php; CurrencyModel.php; ConfigController.php
    - L3 Themes
      - Source: ThemeModel.php
  - L2 Platform Operations
    - L3 Plugins Lifecycle
      - Source: PluginController.php; ServiceProvider/*; app/Plugin hooks
    - L3 Security & Healthcheck
      - Source: SECURITY.md; healthcheck.php; Middleware/*
    - L3 Cronjobs & Jobs Queue
      - Source: CronjobController.php; app/Job/*

- L1 Integration & Extensibility
  - L2 APIs & Events
    - L3 JSON-RPC API
      - Source: jsonrpc.php; app/Api/*
    - L3 Events/Hooks; Subscribers
      - Source: app/Event/*; app/Subscriber/*; EventBuilder/*; custom-hooks/
    - L3 CLI
      - Source: cli; app/Console/*
    - L3 External Links
      - Source: ExternalLink/*; TaskExternalLinkModel/Controller

- L1 Scheduling & Calendar
  - L2 Calendaring & Feeds
    - L3 iCalendar publishing
      - Source: ICalendarController.php

- L1 File & Document Management
  - L2 File Storage & Viewing
    - L3 Avatars
      - Source: AvatarFileModel.php; AvatarFileController.php
    - L3 Project Files
      - Source: ProjectFileModel.php; ProjectFileController.php
    - L3 Task Files & Viewer
      - Source: TaskFileModel.php; FileViewerController.php

- L1 Search & Filtering
  - L2 Discovery & Querying
    - L3 Global & Project Search
      - Source: SearchController.php; app/Filter/*; TaskFinderModel.php
    - L3 Custom Filters
      - Source: CustomFilterModel.php; CustomFilterController.php

## Notes on TOGAF 10 alignment
- The above is a Business Capability Map (L1–L3). L1 = Domains, L2 = Capability groups, L3 = Atomic capabilities.
- Source mapping provides traceability from business capabilities to implementation elements (controllers/models), supporting architecture governance and impact analysis.

## Key Business Objects
- Project, Board (Columns, Swimlanes), Task, Subtask, Comment, Link, File, User, Group, Role/Permission, Tag/Category, Notification, Activity, Analytics (Stats), Settings.

## Non-Functional & Cross-Cutting Concerns
- Security: 2FA, OAuth, Captcha, role-based access, session hardening, healthcheck.
- Extensibility: Plugins, events/hooks, JSON-RPC API, CLI.
- Internationalization: Locale, language packs, timezone/currency.
- Operability: Cronjobs, jobs queue, Docker/compose setups.

## Observed Gaps / Opportunities (from repo scan)
- Portfolio-level planning (programs, objectives, OKRs) is minimal; could be added via plugins.
- Dependency visualization and critical path analytics limited to links; no Gantt out-of-the-box.
- Audit logging and advanced compliance reporting not first-class.
- Webhook endpoints are not explicit in core; plugin ecosystem likely covers it.
- Modern API styles (REST/GraphQL) beyond JSON-RPC could broaden integration options.
