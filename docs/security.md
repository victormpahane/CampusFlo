# Security

## Authentication

Requirements:

- Email/password login
- Secure password handling through a backend provider
- Session management
- Logout
- Password reset
- Email verification if supported

Passwords must never be stored manually in app code or local storage.

Recommended provider:

- Supabase Auth

## Authorization

The app is student-only, but every student must only access their own data.

Required access rules:

- A student can only read and write their own profile
- A student can only read and write their own modules
- A student can only read and write their own timetable
- A student can only read and write their own tasks
- A student can only read and write their own notes
- A student can only read and write their own events

Recommended enforcement:

- Supabase Row Level Security policies

## Data Protection

- Use environment variables
- Do not hardcode API keys
- Do not expose service role keys in frontend code
- Validate and sanitize user input where appropriate
- Use HTTPS for network requests
- Store tokens securely
- Avoid logging sensitive data

## Privacy

Collect only necessary academic productivity data.

Avoid collecting:

- National ID
- Physical home address
- Financial data
- Medical data
- Unnecessary demographic data

## Secure Local Storage

- Do not store passwords locally
- Do not store backend secrets locally
- Scope offline data to the authenticated student
- Clear local user data on logout where required
- Use secure token storage where applicable
