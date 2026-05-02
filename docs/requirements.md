# Requirements

## Product Vision

CampusFlo is a student-only Android, iOS, and web academic companion for tertiary students in Roma, Lesotho. It helps a student manage modules, timetables, labs, practicals, tests, assignments, academic tasks, events, notes, reminders, weekly summaries, and AI-assisted academic planning in one reliable place.

The experience should feel like a smart academic planner rather than a formal school system.

It should help the student answer:

- What classes do I have today?
- What labs or practicals do I have?
- What assignments are due soon?
- What tests are coming?
- What should I prioritize this week?
- What events do I want to attend?
- What notes have I saved?
- Am I overloaded this week?
- What should I focus on first?

## Problem Statement

Tertiary students in Roma, Lesotho often manage academic information through scattered sources such as WhatsApp messages, handwritten notes, class conversations, posters, memory, and informal reminders.

This causes students to:

- Forget tests
- Miss assignment deadlines
- Forget labs and practical sessions
- Lose track of timetable changes
- Miss important events
- Fail to prioritize urgent academic work
- Struggle during busy academic weeks
- Depend too heavily on WhatsApp messages
- Feel academically disorganized

CampusFlo addresses this by giving students one place to organize academic life across Android, iOS, and web.

## Primary User

The only primary user is:

- Student

The student should be able to:

- Create a student profile
- Add modules
- Create a timetable
- Add labs and practicals
- Track tests
- Track assignments
- Track academic tasks
- Save personal events
- Write notes
- Receive reminders
- Use the app offline
- Detect timetable clashes
- Prioritize urgent work
- View weekly academic summaries
- Receive AI-powered academic suggestions
- Use the app on Android, iOS, and web

Every feature should answer this question:

Does this help the student manage academic life better?

## Core Modules

1. Student Profile
2. Modules
3. Timetable
4. Labs and Practicals
5. Tests and Assignments
6. Academic Tasks
7. Events Tracker
8. Notes
9. Notifications
10. AI Communicator
11. Weekly Academic Summary
12. Priority Engine
13. Offline Mode
14. Settings

## Functional Requirements

### Student Profile

Fields:

- Full name
- Institution
- Faculty
- Department
- Programme
- Year of study
- Semester
- Campus or location
- Preferred notification time
- Preferred study style
- Theme preference

These can be free-text values in the MVP, but the system should later support normalized institution, faculty, department, programme, and campus data.

### Modules

Students can add modules with:

- Module code
- Module name
- Lecturer name, optional
- Faculty, optional
- Department, optional
- Semester
- Academic year
- Module color
- Credit value, optional
- Notes

Each module page should later expose:

- Timetable entries
- Labs and practicals
- Upcoming tests
- Upcoming assignments
- Upcoming exams
- Lab reports
- Notes
- Progress context

### Timetable

Each timetable entry includes:

- Module
- Entry type
- Day of week
- Start time
- End time
- Venue
- Reminder setting
- Notes

Supported entry types:

- Lecture
- Tutorial
- Lab
- Practical
- Study Session
- Consultation
- Other

Timetable requirements:

- Daily view
- Weekly view
- Today view
- Next class countdown
- Reminders
- Editing and deletion
- Clash detection

### Labs and Practicals

Labs should not be a completely separate major module in the MVP.

They should exist in two places:

- Timetable entries such as a lab or practical session
- Academic tasks such as a lab report or practical task

### Academic Tasks

Supported task types:

- Test
- Assignment
- Quiz
- Exam
- Presentation
- Lab Report
- Practical Task
- Project Milestone
- Group Work
- Reading Task
- Study Task
- Other

Fields:

- Title
- Module
- Task type
- Due date
- Due time
- Venue, optional
- Priority
- Status
- Description
- Reminder setting
- Estimated workload
- Created at
- Updated at

Supported statuses:

- Not Started
- In Progress
- Almost Done
- Submitted
- Completed
- Missed

Priority levels:

- Low
- Medium
- High
- Critical

### Priority Engine

The priority engine should rank work using:

- Due date
- Task type
- Student-selected priority
- Completion status
- Estimated workload
- Number of tasks in the same week
- Overdue status

Suggested MVP scoring baseline:

- Due today: `+100`
- Due tomorrow: `+80`
- Due this week: `+50`
- Overdue: `+120`
- Priority critical: `+50`
- Priority high: `+30`
- Priority medium: `+15`
- Status not started: `+20`
- Status in progress: `+10`
- Estimated workload high: `+20`

### Events

Students manually add events they care about.

Supported categories:

- Academic
- Social
- Sports
- Religious
- Career
- Workshop
- Study Group
- Personal
- Other

### Notes

Notes should support:

- Creation
- Editing
- Deletion
- Pinning
- Search
- Linking to modules, tasks, or events
- Conversion into tasks, events, or reminders

### AI Communicator

The AI communicator should be rule-based in the MVP and grounded in the student’s actual data.

It should support:

- Deadline reminders
- Class reminders
- Lab reminders
- Weekly summaries
- Task prioritization
- Study suggestions
- Note-to-task conversion suggestions
- Overload warnings
- Clash explanations
- Missed task warnings

### Weekly Academic Summary

The app should generate a weekly summary on Sunday evening or Monday morning, including:

- Class count
- Lab and practical count
- Upcoming tests
- Upcoming assignments
- Upcoming lab reports
- Events
- Most urgent task
- Overdue tasks
- Suggested focus
- Heavy workload warning
- Free time highlights

### Notifications

Notification types:

- Class reminder
- Lab reminder
- Test reminder
- Assignment reminder
- Exam reminder
- Event reminder
- Weekly summary
- Overdue task alert
- Priority suggestion
- AI suggestion
- Clash warning

## Non-Functional Requirements

- Usability: easy for students to use daily
- Mobile-first: Android and iOS should feel natural
- Web support: students can also use the app in a browser
- Offline support: core features must work without internet
- Security: each student must only access their own data
- Privacy: collect only necessary academic data
- Robustness: handle errors and poor network conditions well
- Performance: dashboard should load quickly
- Maintainability: code should stay modular and clean
- Scalability: later support institutions, faculties, departments, and programmes
- Accessibility: text should be readable and UI should stay simple
- Engagement: the product should feel modern and student-friendly

## MVP Scope

Version 1 must include:

- Student registration and login
- Student profile
- Modules
- Timetable
- Labs and practicals as timetable entries
- Timetable clash detection
- Academic tasks
- Tests
- Assignments
- Lab reports
- Priority engine
- Events tracker
- Notes
- Basic AI communicator
- Weekly academic summary
- Local notifications
- Offline viewing
- Offline task and note creation
- Android support
- iOS support
- Web support
- Basic security
- Basic robust error handling

Version 1 excludes:

- Lecturer accounts
- Admin dashboards
- Class rep mode
- Public event approval
- Institution-wide announcements
- Payment features
- Campus map
- Social feed
- Real-time chat
- Advanced AI chatbot
