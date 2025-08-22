Below is a TOGAF-aligned, deduplicated Business Capability hierarchy extracted from the Kanboard source repository. Each Level 1 and Level 2 capability includes direct source-code references. All Level 2 capabilities are decomposed into Level 3 sub-capabilities for comprehensive coverage. This structure is suitable for benchmarking against a Kanboard reference BC set.

## Business Capability Hierarchy

Level 1 BC: Project Management
- Source Reference: app/Model/ProjectModel.php; app/Controller/Project*.php
  - Level 2 BC: Project Lifecycle Management
    - Source Reference: ProjectCreationController.php; ProjectEditController.php; ProjectStatusController.php; ProjectModel.php
    - Level 3:
      - Project Creation and Initialization (ProjectCreationController.php)
      - Project Update and Settings (ProjectEditController.php, ProjectModel.php)
      - Project Activation/Closure (ProjectStatusController.php, ProjectModel.php)
  - Level 2 BC: Project Access and Role Management
    - Source Reference: ProjectPermissionController.php; ProjectRoleController.php; ProjectGroupRoleModel.php; ProjectUserRoleModel.php; ProjectPermissionModel.php; ProjectRoleRestrictionModel.php
    - Level 3:
      - Project Membership and Permissions (ProjectPermissionController.php, ProjectPermissionModel.php)
      - Role Definition and Assignment (ProjectRoleController.php, ProjectGroupRoleModel.php, ProjectUserRoleModel.ph)
      - Role-Based Restrictions (ProjectRoleRestrictionModel.php)
  - Level 2 BC: Project Duplication and Templates
    - Source Reference: ProjectDuplicationModel.php; ProjectActionDuplicationController.php; PredefinedTaskDescriptionController.php; PredefinedTaskDescriptionModel.php
    - Level 3:
      - Project Duplication (ProjectDuplicationModel.php)
      - Action Duplication (ProjectActionDuplicationController.php)
      - Predefined Descriptions/Templates (PredefinedTaskDescription*.php)
  - Level 2 BC: Project Tag Management
    - Source Reference: ProjectTagController.php; TagModel.php; TagDuplicationModel.php
    - Level 3:
      - Tag Creation and Maintenance (ProjectTagController.php, TagModel.php)
      - Tag Duplication Across Projects (TagDuplicationModel.php)
  - Level 2 BC: Project Files Management
    - Source Reference: ProjectFileController.php; ProjectFileModel.php
    - Level 3:
      - Project File Upload/Download (ProjectFileController.php, ProjectFileModel.php)
  - Level 2 BC: Project Activity and Overview
    - Source Reference: ProjectOverviewController.php; ActivityController.php; ProjectActivityModel.php
    - Level 3:
      - Project Overview Dashboard (ProjectOverviewController.php)
      - Project Activity Stream (ActivityController.php, ProjectActivityModel.php)
  - Level 2 BC: Project Notification Management
    - Source Reference: ProjectNotificationModel.php; ProjectNotificationTypeModel.php
    - Level 3:
      - Project Notification Rules (ProjectNotificationModel.php)
      - Notification Types/Channels (ProjectNotificationTypeModel.php)

## Channem Highsess

I have excoluded this, as they need to be marked based
1. Project output.2.System.2.ContextualizeJderor and compared the numberof endusers mrorexul.
3%for forageman to rarrias- blame they girlvi that they were not edited that, from scratch null increaof tQrpW
