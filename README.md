# CampusFlo

CampusFlo is a student-only academic companion for tertiary students in Roma, Lesotho. It supports Android, iOS, and web, and helps students manage modules, timetables, labs, practicals, tests, assignments, academic tasks, events, notes, reminders, weekly summaries, and AI-assisted academic guidance.

## Product Direction

CampusFlo is the project name and platform identity.

The product goal is a Roma-focused student companion that helps a student answer:

- What classes do I have today?
- What labs or practicals do I have?
- What assignments or tests are due soon?
- What should I prioritize this week?
- Am I overloaded right now?
- What should I focus on first?

The MVP is student-only:

- No lecturers
- No admins
- No class reps
- No public event organizers

## Current Foundation

This repository contains the planning and engineering foundation for the app:

- `docs/requirements.md`
- `docs/architecture.md`
- `docs/database-design.md`
- `docs/security.md`
- `docs/testing.md`
- `docs/codex-prompts.md`

## MVP Scope

Version 1 should include:

- Student registration and login
- Student profile setup
- Modules
- Timetable
- Labs and practicals as timetable entries and academic tasks
- Timetable clash detection
- Academic tasks including tests, assignments, exams, and lab reports
- Events tracker
- Notes
- Priority engine
- Weekly academic summary
- Basic AI communicator
- Local notifications
- Offline viewing and offline creation for key items
- Basic security and robust error handling

## Recommended Stack

- Expo React Native
- TypeScript
- Expo Router
- Supabase
- PostgreSQL
- Expo SQLite for offline-first storage

## Build Sequence

1. Scaffold the Expo Router app shell with mock data and modern student-friendly UI.
2. Add shared types, validation, error handling, and defensive rendering.
3. Implement timetable clash detection, priority scoring, and weekly summary logic.
4. Add offline storage and sync queue foundations.
5. Add Supabase authentication, database integration, and Row Level Security.
