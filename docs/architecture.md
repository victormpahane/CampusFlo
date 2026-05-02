# Architecture

## Recommended Stack

- Expo React Native
- TypeScript
- Expo Router
- Supabase
- PostgreSQL
- Local offline storage using Expo SQLite, with AsyncStorage only as a lighter MVP fallback

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

## Design Principles

- Student-only first: every flow is built around a single student managing their own academic life
- Offline-first mindset: core academic flows must remain usable without internet
- Scalable data model: use flexible text fields now, but leave a clean path to normalized academic structures later
- Rule-based intelligence first: AI suggestions should start with deterministic app logic based on student data
- Security by default: authentication, scoped data access, and safe local storage are part of the base architecture

## Scalability Direction

The MVP is generalized for tertiary students in Roma, but the structure must not block future support for:

- Institutions
- Faculties
- Departments
- Programmes
- Campuses
- Different academic years
- Different semester models

Recommended long-term academic hierarchy:

```text
Institution
    Faculty
        Department
            Programme
                Year of Study
                    Semester
                        Modules
```

## Suggested Folder Structure

```text
campusflo/
├── app/
├── components/
│   ├── ui/
│   ├── cards/
│   ├── forms/
│   ├── layout/
│   └── feedback/
├── features/
│   ├── auth/
│   ├── profile/
│   ├── modules/
│   ├── timetable/
│   ├── tasks/
│   ├── events/
│   ├── notes/
│   ├── ai-communicator/
│   ├── notifications/
│   └── offline-sync/
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
