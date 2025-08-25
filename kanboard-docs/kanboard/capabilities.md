# [Kanboard] business capabilities (TOGAF 10 L1-L3)

## Overview
- Repository: https://github.com/kanboard/kanboard
- Primary language: PHP
- Domain: Project and task management with Kanban boards

## L1-L3 capability map
- Level 1 Capability: Project management
  - Level 2 Capability: Board and task organization
    - Level 3 Capability: Board model
      - Evidence: [BoardModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/BoardModel.php), [ColumnModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/ColumnModel.php), [SwimlaneModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/SwimlaneModel.php), [TaskModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskModel.php)
    - Level 3 Capability: Task lifecycle management
      - Evidence: [TaskCreationModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskCreationModel.php), [TaskModificationModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskModificationModel.php), [TaskRecurrenceModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskRecurrenceModel.php), [TaskStatusModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskStatusModel.php), [TaskDuplicationModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/TaskDuplicationModel.php)
    - Level 2 Capability: Task organization
      - Level 3 Capability: Subtask management
        - Evidence: [SubtaskModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/SubtaskModel.php), [SubtaskTimeTrackingModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/SubtaskTimeTrackingModel.php)
      - Level 3 Capability: Tag and category management
        - Evidence: [TagModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/TagModel.php), [CategoryModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/CategoryModel.php)
      - Level 3 Capability: Board configuration
        - Evidence: [ColumnModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/ColumnModel.php), [SswimlaneModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/SwimlaneModel.php)
- Level 1 Capability: User and access management
  - Level 2 Capability: User management
    - Level 3 Capability: Authentication and authorization
      - Evidence: [Auth/](https://github.com/kanboard/kanboard/tree/main/app/Auth)
  - Level 2 Capability: Group and role management
    - Level 3 Capability: Project roles and permissions
      - Evidence: [ProjectPermissionModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectPermissionModel.php), [ProjectRoleModel.phs](https://github.com/kanboard/kanboard/blob/main/app/Model/ProjectRoleModel.php)
- Level 1 Capability: Communication and notification
  - Level 2 Capability: Notification services
    - Level 3 Capability: Email, webhook, RSS notification
      - Evidence: [Notification](https://github.com/kanboard/kanboard/find/main/app/Notification)
- Level 1 Capability: Analytics and reporting
  - Level 2 Capability: Board and task analytics
    - Level 3 Capability: Burndown charts, project daily stats
      - Evidence: [Analytic](https://github.com/kanboard/kanboard/find/main/app/Analytic), [Analytic](https://github.com/kanboard/kanboard/find/main/app/Analytic)
## Capability map
mermaid
  mindmap
    ToGafLhtWaghd
      Kanboard
        Project management
          Board and task organization
            Board model
            Task lifecycle management
            Subtask management
            Tag and category management
            Board configuration
        User and access management
          User management
          Authentication and authorization
          Group and role management
          Project roles and permissions
        Communication and notification
          Notification services
          Email, webhook, RSS notification
        Analytics and reporting
          Board and task analytics