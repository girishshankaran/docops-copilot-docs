# Cisco Social Home (sample UI)

This static HTML page lives in the code repo at `ui/home1.html`. It showcases the Cisco Social experience (posts, quick polls) without any backend.

## How to preview
1. Pull the latest code repo and open `ui/home1.html` directly in a browser (no build needed).
2. Everything is mocked in the file—data loads from inline JavaScript arrays.

## What’s included (at a glance)
- Top toolbar: Posts, Recognition, Quick Poll, Call, Reports.
- Main feed: sample posts and a poll renderer.
- Call modal: simple Webex call launcher with name + email inputs.
- Reports modal: generate department reports with filters, preview results, and download in PDF/XLS.
- Sidebar: Upcoming Events, Job Opportunities, New Hires (with “Wish”), Work Anniversaries, Notifications.

## How to use the page

### Create a post
1. Click **Posts** (top row) to reveal the Post form.
2. Fill Title, Content, Tags (comma separated), and select one or more BUs.
3. Click **Post** to add it to the feed; **Cancel** hides the form and clears inputs.

### Create a quick poll
1. Click **Quick Poll** to open the poll form.
2. Enter the **Poll question**.
3. In **Poll options**, type one option per line.
4. Select one or more BUs (visibility scope).
5. Click **Post** to publish; **Cancel** hides and clears the form.
6. Voting: select an option and submit; results render immediately with percentages. Repeat clicks are blocked per mock “demo-user”.

### Start a call
1. Click **Call** in the toolbar.
2. Enter **Name** and **Email** (both required).
3. Click **Call** to open Webex at `https://cisco.webex.com/meet/gisankar` in a new tab.
4. Use **Cancel** or **×** to close the modal.

### Generate a report
1. Click **Reports** in the toolbar to open the Reports modal.
2. Select a department, report type, date range, and format.
3. Optionally, include moderation details.
4. Click **Preview** to view the generated report data.
5. Click **Download** to save the report in the selected format.
6. View the download history in the modal.

### Sidebar actions
- **Upcoming Events / Job Opportunities:** click **RSVP/Apply** (non-functional stubs).
- **New Hires:** click **Wish** to trigger a “good luck” alert.
- **Work Anniversaries / Notifications:** static list items for now.

## Known limitations (mock state)
- All data is in-memory; refresh resets posts and polls to defaults.
- No persistence, auth, or backend calls.
- Accessibility is minimal (add ARIA and keyboard focus handling before production).
- No analytics or input validation beyond simple required-field checks.

## Notes for engineers
- All styling is inline in `home1.html` (no external assets).
- Scripts are vanilla JS; no external dependencies.
- Accessibility: basic focus/keyboard handling is minimal; add ARIA roles before productionizing.
- Security: the helper `sanitize()` escapes user text when rendering posts/polls.

## Next steps
- Swap mock data with API calls when endpoints are ready.
- Add tests or linting once the page is integrated into the main build pipeline.

## Automated UI Sync Notes

Last synced from `ui/home1.html` at 2026-02-15T11:20:24Z.

### Added UI lines
- `<h1>Cisco Social</h1>`
- Role selector for demo login.
- Reports button in the toolbar.
- Reports modal for generating department reports.

### Removed UI lines
- `<h1>Cisco Social App</h1>`