# Data dictionary

Intended observational unit: a fictional closed software incident.
File: `software_incidents.csv`, UTF-8, comma-separated, header present.
Blank fields mean unrecorded information. Valid values describe the intended
schema; the raw export includes deliberate quality defects.

| Variable | Meaning | Statistical type | Units / valid values |
|---|---|---|---|
| `incident_id` | Incident identifier | Nominal identifier | `INC-001` through `INC-024`; unique after deduplication |
| `service` | Service affected | Nominal categorical | `api`, `web`, `worker`; may be blank |
| `severity` | Ordered operational severity | Ordinal categorical | `low` < `medium` < `high`; distances are not numeric |
| `resolution_hours` | Elapsed opening-to-closure time | Numerical, conceptually continuous | Hours, nonnegative; blank = unknown |
| `deploy_version` | Version at incident opening | Nominal categorical | `v1`, `v2`; not randomized treatment |
| `customer_impact` | Recorded customer impact | Binary categorical | `yes`, `no` |

Rounding duration to whole hours does not make it a count.
Derived in Session 2: `resolution_days = resolution_hours / 24`.
A display label `unknown` for missing service does not recover the true service.
In grouped summaries, `size` counts records; `count` counts nonmissing durations.
