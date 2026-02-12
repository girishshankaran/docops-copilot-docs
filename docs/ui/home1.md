# Cisco Social Home (sample UI)

This static HTML page lives in the code repo at `ui/home1.html`. It showcases the Cisco Social experience (posts, quick polls, groups modal) without any backend.

## How to preview
1. Pull the latest code repo and open `ui/home1.html` directly in a browser (no build needed).
2. Everything is mocked in the file—data loads from inline JavaScript arrays.

## What’s included
- Top toolbar with navigation to Posts, Groups, Recognition, Quick Poll.
- Main feed rendering sample posts and a quick poll with vote handling.
- Groups modal with “New” button, group creation form, and Webex “Meet” buttons (special-case link for “Python Group”).
- Sidebar panels: Upcoming Events, Job Opportunities, New Hires (with “Wish” action), Work Anniversaries, Notifications.

## Notes for engineers
- All styling is inline in `home1.html` (no external assets).
- Scripts are vanilla JS; no external dependencies.
- Accessibility: basic focus/keyboard handling is minimal; add ARIA roles before productionizing.
- Security: the helper `sanitize()` escapes user text when rendering posts/polls.

## Next steps
- Swap mock data with API calls when endpoints are ready.
- Add tests or linting once the page is integrated into the main build pipeline.
