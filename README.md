# CampusFlow

Keep your student life in flow.

CampusFlow is a student-only Android, iOS, and web academic companion for tertiary students in Roma, Lesotho. It helps students manage modules, timetables, labs, tests, assignments, events, notes, reminders, weekly summaries, and AI-powered academic guidance. It is designed using Expo React Native and TypeScript, with a structure that can later scale across faculties, departments, programmes, institutions, and campuses.

## Current Foundation

This repository currently contains product and engineering foundation documents derived from the locked project direction:

- `docs/requirements.md`
- `docs/architecture.md`
- `docs/database-design.md`
- `docs/security.md`
- `docs/testing.md`
- `docs/codex-prompts.md`

## MVP Focus

The MVP centers on a single user role:

- Student

Core MVP areas:

- Student profile
- Modules
- Timetable
- Labs/practicals as timetable entries and academic tasks
- Academic tasks
- Events
- Notes
- Weekly summary
- Priority engine
- Basic AI communicator
- Notifications
- Offline support
- Security and robustness baseline

## Recommended Stack

- Expo React Native
- TypeScript
- Expo Router
- Supabase
- PostgreSQL
- Expo SQLite or AsyncStorage for offline data

## Next Build Steps

1. Scaffold the Expo TypeScript app with Expo Router.
2. Implement the UI shell with mock data.
3. Add shared types, validation, and defensive utilities.
4. Implement clash detection, priority scoring, and weekly summary logic.
5. Add Supabase auth and row-level security later.
