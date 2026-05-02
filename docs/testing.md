# Testing

## Minimum Test Areas

- Authentication flow
- Profile creation
- Module creation
- Timetable entry creation
- Timetable clash detection
- Task creation
- Priority scoring
- Offline task creation
- Sync queue behavior
- Notification scheduling
- Weekly summary generation

## Robustness Requirements

### Network Failure

The app should:

- Show offline status
- Save changes locally
- Queue unsynced changes
- Retry failed syncs
- Notify the user when sync succeeds or fails

### Error Handling

Handle failures such as:

- Failed login
- Failed signup
- Failed sync
- Invalid timetable time
- Invalid due date
- Missing module
- Duplicate task
- Clashing timetable entry
- Failed notification scheduling

### Data Validation

Validate before save:

- End time must be after start time
- Task due date cannot be empty
- Module name cannot be empty
- Reminder time must be valid
- Priority must be allowed
- Status must be allowed

### Crash Prevention

Use:

- TypeScript types
- Default values
- Defensive UI rendering
- Error boundaries where appropriate
- Form validation
- Safe date parsing
- Safe notification scheduling
