# Architecture

## Recommended Stack

- Expo React Native
- TypeScript
- Expo Router
- Supabase
- PostgreSQL
- Local offline storage using Expo SQLite or AsyncStorage

## High-Level Architecture

```text
Android / iOS / Web App
        |
        v
Expo React Native Frontend
        |
        |---- Local Offline Storage
        |       - Modules
        |       - Timetable
        |       - Tasks
        |       - Events
        |       - Notes
        |       - Sync Queue
        |
        v
Supabase
        |
        |---- Authentication
        |---- PostgreSQL Database
        |---- Row Level Security
        |---- Cloud Sync
        |
        v
AI Communicator Logic
        |
        |---- Priority Engine
        |---- Weekly Summary Generator
        |---- Reminder Generator
        |---- Note-to-task Suggestions
```

## Scalability Direction

The MVP is student-only, but the data model and app structure must not block later support for:

- Institutions
- Faculties
- Departments
- Programmes
- Campuses
- Different semester models

Use flexible fields in the MVP, with a path to normalized reference tables later.

## Suggested Folder Structure

```text
campusflow/
├── app/
├── components/
├── features/
├── lib/
├── types/
├── constants/
├── hooks/
├── assets/
├── docs/
└── README.md
```

## Planned Delivery Phases

1. Requirements and design
2. Project setup
3. Authentication and profile
4. Modules
5. Timetable and labs
6. Academic tasks
7. Events and notes
8. AI communicator
9. Offline mode and sync
10. Security, robustness, and testing
