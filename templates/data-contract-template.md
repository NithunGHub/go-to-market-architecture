# Data Contract Template

Copy this file for every integration in the stack. A sync nobody documented is a sync nobody can fix.

## Integration: `<name>`

| Field | Value |
|-------|-------|
| Source system | |
| Target system | |
| Direction | One-way / bidirectional (note: bidirectional on the same fields is discouraged) |
| Objects synced | e.g., Lead, Contact, Campaign Member |
| Trigger / frequency | Real-time webhook / every 15 min / nightly batch |
| Owner | Name and team |
| Created / last reviewed | |

## Field map

| Source field | Target field | Transformation | Conflict rule (which wins) |
|--------------|-------------|----------------|---------------------------|
| | | | |
| | | | |

Rules:
- One writer per field. If both systems write to the same field, you have a race condition, not automation.
- Never overwrite a human-entered value with an automated guess unless the contract says so explicitly.

## Filters

Which records sync? Write the criteria exactly (e.g., "Leads where Lead Source = Web and Country in (US, CA, GB)").

## Error handling

- Where do failures go? (Queue name, channel, owner)
- Retry policy:
- Who is paged on sustained failure?

## Monitoring

- Health check: (dashboard link or query)
- Expected volume per day:
- Alert threshold:

## Change log

| Date | Change | Author |
|------|--------|--------|
| | | |
