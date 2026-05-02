# Codex Prompts

## Prompt 1: UI Shell

```text
Create an Expo React Native TypeScript app called CampusFlo.

CampusFlo is a student-only academic productivity platform for tertiary students in Roma, Lesotho. It must support Android, iOS, and web.

Core requirements:
- Use Expo React Native with TypeScript.
- Use Expo Router for navigation.
- Create a clean, scalable folder structure.
- Add bottom tab navigation with Home, Timetable, Tasks, Events, and AI.
- Add secondary screens for Modules, Notes, Weekly Summary, Profile Setup, and Settings.
- Use a modern student-friendly UI with rounded cards, readable typography, module color tags, and dark/light theme readiness.
- Use mock data for now.
- Do not implement backend yet.
- Do not implement authentication yet.
- Focus on clean architecture, reusable components, and attractive UI.

Screens to create:
- Welcome
- Login placeholder
- Register placeholder
- Home Dashboard
- Timetable
- Modules
- Tasks
- Events
- Notes
- AI Communicator
- Weekly Summary
- Settings

Home Dashboard should show:
- Greeting
- Next class or lab
- Today’s timetable
- Urgent academic task
- Upcoming event
- AI suggestion card
- Quick add button

Timetable screen should support mock entries of types:
- Lecture
- Tutorial
- Lab
- Practical
- Study Session

Tasks screen should support mock academic task types:
- Test
- Assignment
- Exam
- Lab Report
- Practical Task
- Presentation
- Project Milestone

Create reusable components:
- AppCard
- AppButton
- SectionHeader
- EmptyState
- StatusBadge
- PriorityBadge
- TimetableCard
- TaskCard
- EventCard
- AiSuggestionCard

Keep the code modular and ready for future backend, offline sync, security, and notifications.
```

## Prompt 2: Security and Robustness Foundation

```text
Add a security and robustness foundation to the CampusFlo app.

Requirements:
- Create TypeScript types for StudentProfile, Module, TimetableEntry, AcademicTask, Event, Note, Notification, and AppSettings.
- Add validation helpers for forms.
- Add safe date/time utility functions.
- Add error handling utilities.
- Add a reusable ErrorMessage component.
- Add a reusable LoadingState component.
- Add a reusable OfflineBanner component.
- Add placeholder online/offline detection hook called useOnlineStatus.
- Add placeholder sync status types: synced, pending_create, pending_update, pending_delete, failed.
- Add defensive rendering so screens do not crash when mock data is missing.
- Do not add backend yet.
- Keep everything modular and production-friendly.
```

## Prompt 3: Priority and Clash Logic

```text
Implement the first business logic utilities for CampusFlo.

Add:
1. Timetable clash detection
2. Academic task priority scoring
3. Weekly academic summary generation

Requirements:
- Create lib/clashDetection.ts.
- Create lib/priorityEngine.ts.
- Create lib/weeklySummary.ts.
- Clash detection should identify overlapping timetable entries on the same day.
- Priority engine should score academic tasks based on due date, selected priority, status, and estimated workload.
- Weekly summary should count classes, labs/practicals, tests, assignments, lab reports, events, and overdue tasks.
- Add sample usage on the Home Dashboard using mock data.
- Keep all functions pure and testable.
```
