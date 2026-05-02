# Database Design

## Main Tables

- `student_profiles`
- `modules`
- `timetable_entries`
- `academic_tasks`
- `events`
- `notes`
- `notifications`
- `weekly_summaries`
- `app_settings`
- `sync_queue`

## Future Reference Tables

- `institutions`
- `faculties`
- `departments`
- `programmes`
- `campuses`

## student_profiles

- `id`
- `user_id`
- `full_name`
- `institution_name`
- `faculty_name`
- `department_name`
- `programme_name`
- `campus_name`
- `year_of_study`
- `semester`
- `created_at`
- `updated_at`

## modules

- `id`
- `user_id`
- `module_code`
- `module_name`
- `lecturer_name`
- `faculty_name`
- `department_name`
- `programme_name`
- `semester`
- `academic_year`
- `color`
- `credits`
- `notes`
- `created_at`
- `updated_at`
- `deleted_at`

## timetable_entries

- `id`
- `user_id`
- `module_id`
- `entry_type`
- `day_of_week`
- `start_time`
- `end_time`
- `venue`
- `reminder_minutes_before`
- `notes`
- `created_at`
- `updated_at`
- `deleted_at`
- `sync_status`

Allowed `entry_type` values:

- `lecture`
- `tutorial`
- `lab`
- `practical`
- `study_session`
- `consultation`
- `other`

## academic_tasks

- `id`
- `user_id`
- `module_id`
- `title`
- `task_type`
- `due_date`
- `due_time`
- `venue`
- `priority`
- `status`
- `description`
- `estimated_workload`
- `reminder_days_before`
- `priority_score`
- `created_at`
- `updated_at`
- `deleted_at`
- `sync_status`

Allowed `task_type` values:

- `test`
- `assignment`
- `quiz`
- `exam`
- `presentation`
- `lab_report`
- `practical_task`
- `project_milestone`
- `group_work`
- `reading_task`
- `study_task`
- `other`

## events

- `id`
- `user_id`
- `title`
- `description`
- `event_date`
- `start_time`
- `end_time`
- `venue`
- `category`
- `status`
- `reminder_minutes_before`
- `notes`
- `created_at`
- `updated_at`
- `deleted_at`
- `sync_status`

## notes

- `id`
- `user_id`
- `module_id`
- `task_id`
- `event_id`
- `title`
- `content`
- `pinned`
- `converted_to_task`
- `created_at`
- `updated_at`
- `deleted_at`
- `sync_status`

## notifications

- `id`
- `user_id`
- `title`
- `message`
- `notification_type`
- `scheduled_for`
- `sent`
- `read`
- `related_entity_type`
- `related_entity_id`
- `created_at`
- `updated_at`

## weekly_summaries

- `id`
- `user_id`
- `week_start_date`
- `week_end_date`
- `summary_text`
- `urgent_task_id`
- `class_count`
- `lab_count`
- `test_count`
- `assignment_count`
- `event_count`
- `created_at`
- `updated_at`

## app_settings

- `id`
- `user_id`
- `class_reminder_minutes`
- `lab_reminder_minutes`
- `test_reminder_days`
- `assignment_reminder_days`
- `event_reminder_minutes`
- `weekly_summary_enabled`
- `ai_suggestions_enabled`
- `theme`
- `created_at`
- `updated_at`

## sync_queue

- `id`
- `user_id`
- `entity_type`
- `entity_id`
- `operation`
- `payload`
- `sync_status`
- `attempt_count`
- `last_attempt_at`
- `error_message`
- `created_at`
- `updated_at`

Allowed `sync_status` values:

- `synced`
- `pending_create`
- `pending_update`
- `pending_delete`
- `failed`

## Conflict Handling

MVP conflict rule:

- Prefer latest `updated_at`
- If conflict is unclear, keep the local copy and warn the user
