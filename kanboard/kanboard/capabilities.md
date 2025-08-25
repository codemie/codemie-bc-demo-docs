# Kanboard business capabilities (KANBOORD kanban project management) (TOGAF 10 L1$—L3)

## Overview
- Repository: https://github.com/kanboard/kanboard
- Primary language: PHP
~ Domain: Self-hosted Kanban project management platform

## L1$—L3 capability map
- Level 1 Capability: Work management
  - Level 2 Capability: Board and workflow management
    - Level 3 Capability: Columns and swimlanes
      - Evidence: [ColumnModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/ColumnModel.php), [SwimlaneModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/SwimlaneModel.php)
    - Level 3 Capability: Transitions and restrictions
      - Evidence: [TransitionModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/TransitionModel.php), [ColumnMoveRestrictionModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/ColumnMoveRestrictionModel.php), [ColumnRestrictionModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/ColumnRestrictionModel.php)
  - Level 2 Capability: Task management
    - Level 3 Capability: Creation and modification
      - Evidence: [TaskCreationModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskCreationModel.php), [TaskModificationModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskModificationModel.php)
    - Level 3 Capability: Subtasks and time tracking
      - Evidence: [SubtaskModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/SubtaskModel.php), [SubtaskTimeTrackingModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/SubtaskTimeTrackingModel.php)
    - Level 3 Capability: Tags and categories
      - Evidence: [TagModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/TagModel.php), [CategoryModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/CategoryModel.php)
    - Level 3 Capability: Attachments and external links
      - Evidence: [TaskFileModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskFileModel.php), [TaskExternalLinkModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskExternalLinkModel.php)
    - Level 3 Capability: Recurrence and duplication
      - Evidence: [TaskRecurrenceModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskRecurrenceModel.php), [TaskDuplicationModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskDuplicationModel.php)
- Level 1 Capability: Collaboration
  - Level 2 Capability: Comments
    - Level 3 Capability: Task comments
      - Evidence: [CommentModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/CommentModel.php)
  - Level 2 Capability: Notifications
    - Level 3 Capability: User and project notifications
      - Evidence: [NotificationModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/NotificationModel.php), [ProjectNotificationModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectNotificationModel.php)
- Level 1 Capability: User and access management
  - Level 2 Capability: User accounts and roles
    - Level 3 Capability: User lifecycle management
      - Evidence: [UserModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/UserModel.php), [LastLoginModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/LastLoginModel.php), [PasswordResetModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/PasswordResetModel.php), [RememberMeSessionModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/RememberMeSessionModel.php)
  - Level 2 Capability: Groups and permissions
    - Level 3 Capability: Group and project roles and permissions
      - Evidence: [GroupModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/GroupModel.php), [GroupMemberModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/GroupMemberModel.php), [ProjectPermissionModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectPermissionModel.php), [ProjectGroupRoleModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectGroupRoleModel.php)
- Level 1 Capability: Analytics and reporting
  - Level 2 Capability: Project stats and task analytics
    - Level 3 Capability: Daily stats analytics and column stats
      - Evidence: [ProjectDailyStatsModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectDailyStatsModel.php), [ProjectDailyColumnStatsModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectDailyColumnStatsModel.php), [TaskAnalyticModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskAnalyticModel.php)
- Level 1 Capability: Configuration and administration
  - Level 2 Capability: Settings, theme, localization, schema
    - Level 3 Capability: Settings and theme
      - Evidence: [SettingModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/SettingModel.php), [ThemeModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/ThemeModel.php)
    - Level 3 Capability: Localization and schema
      - Evidence: [Locale directory](https://github.com/kanboard/kanboard/tree/main/app/Locale), [TimezoneModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/TimezoneModel.php), [LanguageModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/LanguageModel.php), [Schema directory](https://github.com/kanboard/kanboard/tree/main/app/Schema)
- Level 1 Capability: Integration and API
  - Level 2 Capability: JSON RPC, CLI, Plugins, import and export
    - Level 3 Capability: JSONRPC and CLI
      - Evidence: [jsonrpc.php](https://github.com/kanboard/kanboard/blob/main/jsonrpc.php), [cli](https://github.com/kanboard/kanboard/blob/main/cli)
    - Level 3 Capability: Plugins
      - Evidence: [plugins directory](https://github.com/kanboard/kanboard/tree/main/plugins)
    - Level 3 Capability: Import and export
      - Evidence: [Import directory](https://github.com/kanboard/kanboard/tree/main/app/Import), [Export directory](https://github.com/kanboard/kanboard/tree/main/app/Export)
- Level 1 Capability: Automation
  - Level 2 Capability: Actions and triggers, event handling
    - Level 3 Capability: Actions and triggers
      - Evidence: [ActionModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/ActionModel.php)
    - Level 3 Capability: Event handling
      - Evidence: [Event directory](https://github.com/kanboard/kanboard/tree/main/app/Event), [EventBuilder directory](https://github.com/kanboard/kanboard/tree/main/app/EventBuilder)
- Level 1 Capability: Security and audit
  - Level 2 Capability: Captcha, last login, user locking
    - Level 3 Capability: Captcha and user locking
      - Evidence: [CaptchaModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/CaptchaModel.php), [UserLockingModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/UserLockingModel.php), [LastLoginModel.php](https://github.com/kanboard/kanboard/blob/main/app/Model/LastLoginModel.php)
- Level 1 Capability: UI and templates
  - Level 2 Capability: Templates, formatting, pagination, filtering
    - Level 3 Capability: Templates and formatting
      - Evidence: [Template directory](https://github.com/kanboard/kanboard/tree/main/app/Template, [Formatter directory](https://github.com/kanboard/kanboard/tree/main/app/Formatter)
    - Level 3 Capability: Pagination and filtering
      - Evidence: [Pagination directory](https://github.com/kanboard/kanboard/tree/main/app/Pagination), [Filter directory](https://github.com/kanboard/kanboard/tree/main/app/Filter)

### Capability map

`[[mermaid]]

mindmap
  root
    Work management
      Board and workflow management
        Columns and swimlanes
        Transitions and restrictions
      Task management
        Creation and modification
        Subtasks and time tracking
        Tags and categories
        Attachments and external links
        Recurrence and duplication
      Collaboration
        Comments
        Notifications
      User and access management
        Accounts and roles
        Groups and permissions
    Analytics and reporting
      Project stats
      Task analytics
    Configuration and administration
      Settings and theme
      Localization and schema
    Integration and API
      JSON RPC and CLI
      Plugins
      Import and export
    Automation
      Actions and triggers
      Event handling
    Security and audit
      Captcha and user locking
      Last login tracking
    UI and templates
      Templates and formatting
      Pagination and filtering

``]-]
