# SPL Search Foundations

This module focused on using SPL to explore Windows System Event Logs that were already being ingested into Splunk.

## What I Learned

- How to search a specific index and sourcetype.
- Why the selected time range affects search results.
- How to inspect important fields such as:
  - `_time`
  - `host`
  - `source`
  - `sourcetype`
  - `EventCode`
  - `SourceName`
  - `Message`
- How to summarize events with `stats`.
- How to sort and display useful fields with `sort` and `table`.
- Why a frequently occurring event is not automatically suspicious.

## Lab

I used the existing Windows System Event Logs in Splunk and practiced:

- Listing Windows System events.
- Counting events by `EventCode`.
- Selecting one EventCode and reviewing its provider and message.
- Comparing results across different time ranges.

## Queries

- `queries/08-basic-spl.spl`

## Evidence

- `screenshots/08-eventcode-statistics.png`
- `screenshots/08-event-detail.png`
