# API

Placeholder API documentation.

## Report Summary

The `ReportSummary` interface defines the structure of a report summary object.

### Properties
- `id`: string - Unique identifier for the report.
- `name`: string - Name of the report.
- `createdAt`: string - Timestamp indicating when the report was created in ISO 8601 format.

## List Reports

The `listReports` function retrieves an array of report summaries.

### Returns
- An array of `ReportSummary` objects.
- Example output:
  - `id`: 'rpt-001'
  - `name`: 'Weekly Operations'
  - `createdAt`: '2026-02-16T00:00:00Z'