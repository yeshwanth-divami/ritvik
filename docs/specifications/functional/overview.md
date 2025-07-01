
# Functional Overview (v1)

## Primary Commands (Google Chat Slash Commands)
- `/task`: Trigger task creation. Will optionally invoke a pop-up dialog to input task details.
- `/update`: Allow users to update existing tasks. Dialog may prompt for task ID and new status or description.
- `/close`, `/reassign`, `/status`, etc.: To be explored for deeper workflow support.

## Minimum Task Object Schema
- Task ID (auto-generated)
- Title
- Created By
- Description (optional)
- Assigner (optional, defaults to the creator)
- Assignee
- Status
- Created On
- Deadline (optional)

## Interface Modes
 1. **Slash Command Input:** Direct use of chat slash commands with structured natural language or pre-defined formats.
 2. **Form Dialog:** Auto-triggered modal dialog with input fields for structured entry (task name, assignee, deadline, description).

## Planned System Behavior
- All tasks are logged in a centralized PostgreSQL database hosted on Diwami infrastructure.
- Assigned tasks will be visible only to the relevant participants in Google Chat; full visibility through the web UI.
- UI version will allow full CRUD operations and historical analytics.
- Metric tracking planned: average closure time, open tasks by person, overdue metrics, etc.
