# Cisco Social Home (sample UI)

This static HTML page lives in the code repo at `ui/home1.html`. It showcases the Cisco Social experience (posts, quick polls, groups modal) without any backend.

## How to preview
1. Pull the latest code repo and open `ui/home1.html` directly in a browser (no build needed).
2. Everything is mocked in the file—data loads from inline JavaScript arrays.

## What’s included (at a glance)
- Top toolbar: Posts, Groups, Recognition, Quick Poll.
- Main feed: sample posts and a poll renderer.
- Groups modal: list + create, with Webex “Meet” buttons (special-case link for “Python Group”).
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

### Manage groups
1. Click **Groups** to open the modal.
2. To view a group: click its name to see members and a **Meet** button.
3. To start a meeting: click **Meet** (Python Group always routes to `https://cisco.webex.com/meet/gisankar`; others use the group’s Webex link).
4. To create a group:
   - Click **New**.
   - Enter **Group Name** and **Criteria** (comma-separated skills/departments).
   - Submit to auto-populate members whose skills match the criteria; a Webex link is generated from the name (or the Python Group special-case link).

### Recognition (placeholder)
- Click **Recognition** to see the current placeholder alert (“coming soon”).

### Sidebar actions
- **Upcoming Events / Job Opportunities:** click **RSVP/Apply** (non-functional stubs).
- **New Hires:** click **Wish** to trigger a “good luck” alert.
- **Work Anniversaries / Notifications:** static list items for now.

## Known limitations (mock state)
- All data is in-memory; refresh resets posts, polls, and groups to defaults.
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
