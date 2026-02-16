# Documentation Style Guide
- Keep language concise and task-focused.
- Use present tense, active voice.
- Headings sentence case; code in backticks.
- Prefer bullet lists over long paragraphs.

## API Reference

### Report Summary
- `id`: string - Unique identifier for the report.
- `name`: string - Name of the report.
- `createdAt`: string - Timestamp of report creation in ISO 8601 format.
- `category`: 'operations' | 'security' | 'compliance' - Category of the report.

### Functions

#### `listReports`
- Returns an array of `ReportSummary` objects.
- Example output:
  - `id`: 'rpt-001'
  - `name`: 'Weekly Operations'
  - `createdAt`: '2026-02-16T00:00:00Z'
  - `category`: 'operations'

#### `getReportById`
- Returns a `ReportSummary` object or `undefined` if not found.
- Accepts:
  - `id`: string - Unique identifier for the report.