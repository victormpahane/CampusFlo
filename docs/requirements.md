# Requirements

## Product Vision

CampusFlow is a student-only Android, iOS, and web academic companion for tertiary students in Roma, Lesotho. It helps students manage modules, timetables, labs, tests, assignments, events, notes, reminders, weekly summaries, and AI-powered academic guidance.

It should help a student answer:

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

Students often manage academic information through scattered sources such as WhatsApp, handwritten notes, conversations, posters, and memory. This leads to missed deadlines, forgotten labs, timetable confusion, poor prioritization, and academic disorganization.

CampusFlow addresses this by giving students one reliable place to manage academic life.

## Primary User

The only user in the MVP is:

- Student

The student should be able to:

- Create a student profile
- Add modules
- Create a timetable
- Add labs and practicals
- Track tests and assignments
- Track academic tasks
- Save personal events
- Write notes
- Receive reminders
- Use the app offline
- Detect timetable clashes
- Prioritize urgent work
- View weekly academic summaries
- Receive AI-powered academic suggestions
- Use Android, iOS, and web

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
- Campus/location
- Preferred notification time
- Preferred study style
- Theme preference

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

Each module should expose linked timetable entries, tasks, notes, and progress context.

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

### Labs

Labs are not a standalone major module in MVP. They appear as:

- Timetable entries
- Academic tasks such as lab reports

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

Statuses:

- Not Started
- In Progress
- Almost Done
- Submitted
- Completed
- Missed

Priorities:

- Low
- Medium
- High
- Critical

### Events

Students manually add events they care about.

Categories:

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

Notes support:

- Creation
- Editing
- Deletion
- Pinning
- Search
- Linking to modules/tasks/events
- Conversion into task/event/reminder

### AI Communicator

The AI communicator should be rule-based in MVP and grounded in real student data. It should support:

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
- Lab/practical count
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

### Offline Mode

Core offline support must allow:

- Viewing modules, timetable, tasks, events, and notes
- Creating notes, tasks, and timetable entries
- Local reminders
- Sync queueing for cloud sync on reconnect

## Non-Functional Requirements

- Usability
- Mobile-first design
- Web support
- Offline support
- Security
- Privacy
- Robustness
- Performance
- Maintainability
- Scalability
- Accessibility
- Engagement

## MVP Scope

Included:

- Registration and login
- Student profile
- Modules
- Timetable
- Labs/practicals through timetable and tasks
- Clash detection
- Academic tasks
- Events
- Notes
- Basic AI communicator
- Weekly summary
- Local notifications
- Offline viewing
- Offline task and note creation
- Android, iOS, and web support
- Basic security and error handling

Excluded:

- Lecturer accounts
- Admin dashboards
- Public event approvals
- Institution-wide announcements
- Payments
- Campus map
- Chat
- Social feeds
- Advanced AI chatbot
