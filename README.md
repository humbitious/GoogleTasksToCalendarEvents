# GoogleTasksToCalendarEvents
This google action script adds new google tasks that have due dates to the local Noon time of the duedate with a duration equal to the calendar's default.

# Google Tasks to Calendar Sync

This Google Apps Script automatically syncs tasks from Google Tasks to Google Calendar. It creates calendar events for tasks with due dates, setting them at noon on the due date.

## Features

- Automatically syncs new or updated tasks from Google Tasks to Google Calendar
- Creates calendar events for tasks with due dates
- Sets calendar events at noon on the task's due date
- Only processes uncompleted tasks
- Runs automatically every 5 minutes
- Avoids creating duplicate events

## Prerequisites

- A Google account
- Access to Google Tasks and Google Calendar
- Basic familiarity with Google Apps Script

## Installation

1. Open [Google Apps Script](https://script.google.com/) in your browser.
2. Click on "New project" to create a new script.
3. Delete any existing code in the script editor.
4. Copy the entire script from the `script.gs` file in this repository and paste it into the script editor.
5. Replace the following variables with your own values:
   - `taskListId`: Your Google Tasks list ID
   - `calendarId`: Your Google Calendar ID
6. Save the script (File > Save or Ctrl/Cmd + S).

## Setup

1. Run the `createTrigger` function:
   - Select `createTrigger` from the function dropdown at the top of the script editor.
   - Click the "Run" button (play icon).
2. The first time you run the script, you'll be prompted to authorize it. Follow the prompts to grant the necessary permissions.

## Usage

After setup, the script will run automatically every 5 minutes. It will:
- Check for new or updated tasks in your specified Google Tasks list
- Create calendar events for tasks with due dates that haven't been synced yet
- Log information about the process, including which tasks were processed and why

You don't need to do anything else - the sync will happen automatically.

## Customization

- To change how often the script runs, modify the `everyMinutes(5)` line in the `createTrigger` function.
- To change the time of day when events are created, modify the `setHours(12, 0, 0, 0)` line in the `createCalendarEvent` function.

## Troubleshooting

If you encounter any issues:
1. Check the execution logs in the Google Apps Script editor (View > Logs).
2. Ensure you've correctly set your Task List ID and Calendar ID.
3. Verify that your Google account has the necessary permissions for both Tasks and Calendar.

## Contributing

Contributions to improve the script are welcome. Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
