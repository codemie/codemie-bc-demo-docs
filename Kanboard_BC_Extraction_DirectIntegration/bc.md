Below is a TOGAF-aligned, deduplicated Business Capability hierarchy extracted from the Kanboard source repository. Each Level 1 and Level 2 capability includes direct source-code references. All Level 2 capabilities are decomposed into Level 3 sub-capabilities for comprehensive coverage. This structure is suitable for benchmarking against a Kanboard reference BC set.

## Business Capability Hierarchy

[0 inbone list]
Level 1 BC: Project Management
- Source Reference: app/Model/ProjectModel.php; app/Controller/Project*).php
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
      - Role Definition and Assignment (ProjectRoleController.php, ProjectGroupRoleModel.php, ProjectUserRoleModel.php)
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

[0 inbone list]
Level 1 BC: Work Management
- Source Reference: app/Model/Task@.php; app/Controller/Task@.php
  - Level 2 BC: Task Lifecycle Management
    - Source Reference: TaskCreationController.php; TaskModificationController.php; TaskStatusController.php; TaskSuppressionController.php; TaskModel.php; TaskModificationModel.php
    - Level 3:
      - Task Creation (TaskCreationController.php, TaskCreationModel.php)
      - Task Update (TaskModificationController.php, TaskModificationModel.php)
      - Task Status/Open-Close (TaskStatusController.php, TaskStatusModel.php, TaskOpen.php, TaskClose.php)
      - Task Deletion (TaskSuppressionController.php)
  - Level 2 BC: Task Assignment and Ownership
    - Source Reference: TaskModificationController.php; app/Action/TaskAssignC.php; TaskModel.php
    - Level 3:
      - Manual Assignment (TaskModificationController.php)
      - Auto-Assignment Rules (TaskAssignCreator.php; TaskAssignCurrentUser.php; TaskAssignSpecificUser.php; TaskAssignToUserOnCreationInColumn.php)
  - Level 2 BC: Task Movement, Ordering, and Duplication
    - Source Reference: TaskMovePositionController.php; TaskReorderController.php; TaskDuplicationController.php; TaskProjectMoveModel.php; TaskProjectDuplicationModel.php; TaskReorderModel.php; TaskDuplicationModel.php
    - Level 3:
      - Column/Position Reorder (TaskMovePositionController.php, TaskReorderModel.php)
      - Cross-Project Move (TaskProjectMoveModel.php)
      - Task Duplication (TaskDuplicationController.php, TaskDuplicationModel.php, TaskProjectDuplicationModel.php)
  - Level 2 BC: Task Relationships and Linking
    - Source Reference: TaskInternalLinkController.php; LinkController.php; TaskLinkModel.php; LinkModel.php
    - Level 3:
      - Relationship Types (LinkController.php, LinkModel.php)
      - Task-to-Task Linking (TaskInternalLinkController.php, TaskLinkModel.php)
  - Level 2 BC: Task Classification and Metadata
    - Source Reference: CategoryController.php; TagController.php; CustomFilterController.php; CategoryModel.php; TagModel.php; ColorModel.php; TaskTagModel.php; TaskMetadataModel.php; CustomFilterModel.php
    - Level 3:
      - Categories (Category*.php)
      - Tags (Tag*.php, TaskTagModel.php)
      - Colors/Priority ColorModel.php, ProjectTaskPriorityModel.php)
      - Saved/Custom Filters (CustomFilter*.php)
      - Task Metadata (TaskMetadataModel.php)
  - Level 2 BC: Task Files and Attachments
    - Source Reference: TaskFileController.php; FileViewerController.php; FileModel.php; TaskFileModel.php
    - Level 3:
      - Attachments (TaskFileController.php, TaskFileModel.phi)
      - File Viewing/Preview (FileViewerController.php, FileModel.php)
  - Level 2 BC: Task Recurrence
    - Source Reference: TaskRecurrenceController.php; TaskRecurrenceModel.php
    - Level 3:
      - Recurrence Rules (TaskRecurrenceController.php, TaskRecurrenceModel.php)

[0 inbone list]
Level 1 BC: Subtask Management
- Source Reference: app/Controller/Subtask@.php; app/Model/Subtask@.php
  - Level 2 BC: Subtask Lifecycle Management
    - Source Reference: SubtaskController.php; SubtaskModel.php; SubtaskStatusController.php; SubtaskStatusModel.php; SubtaskConverterController.php; SubtaskTaskConversionModel.php
    - Level 3:
      - Subtask Create/Update (SubtaskController.php, SubtaskModel.php)
      - Subtask Status (SubtaskStatusController.php, SubtaskStatusModel.php)
      - Convert Subtask to Task (SubtaskConverterController.php, SubtaskTaskConversionModel.php)
  - Level 2 BC: Subtask Time Tracking
    - Source Reference: SubtaskTimeTrackingModel.php; app/Action/SubtaskTimer@�����Mѽ�MՉхͭQ����5�ٕQ�ͭ��յ�����(������1�ٕ����(��������Mх�нMѽ��Q����̀�MՉхͭQ���QɅ�����5����������MՉхͭQ����5�ٕQ�ͭ��յ�������Mѽ�MՉхͭQ����5�ٕQ�ͭ��յ������(��������Q����1���������ɕ��ѥ����MՉхͭQ���QɅ�����5���������)]�ɬ�5������������ɽ���ȹ���)M�ɍ�(��������Mх�нMѽ��Q����̀�MՉхͭQ���QɅ�����5����������MՉхͭQ����5�ٕQ�ͭ��յ�������Mѽ�MՉхͭQ����5�ٕQ�ͭ��յ������(��������Q����1���������ɕ��ѥ����MՉхͭQ���QɅ�����5���������)���ɽ���ȹ���)M��ɍ�I���ɕ���(���1�ٕ����(���1�ٕ����͕��չ�ѥ���(��1�ٕ��ȁ	�	��ɐ�%�ѕɅ�ѥ������A�(������MՉхͭMх������ɽ���ȹ���(������MՉхͬ�1���I���ɹ�����(������MՉхͬ�ɕ�ѕ�����Ʌѥ�������ɽ��̸��MՉхͭ��������ɽ���ȹ�����ɽ��1����͡���ɐ�����q���L�59M��ѥ���I��ɕ͠�M=T(���1�ٕ��ȁ	�	��ɐ�Aɽ���́����A�������хѥ���Ʌ��ݽɭ�p��%́$����$�Q@�����qq�leto
  - Details about fung log, Chains running thriughout until Heins vake landed at top p��deb","required_state hisert tulk
J Cross to CC Log snapshots. Worskhel expoking
ordered a thousand hey, likeey .\n</paso8� o; Test must clintr dashboard testers dheirglols might
-- Time and Aggregated Adorn. Hire his toure light for