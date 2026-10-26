# Data dictionary

Intended observational unit: a fictional closed software incident.
File: `software_incidents.csv`, UTF-8, comma-separated, header present.
Blank fields mean unrecorded information. Valid values describe the intended
schema; the raw export includes deliberate quality defects.

| Variable | Meaning | Statistical type | Units / valid values |
| --- | --- | --- | --- |
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

## Deployment benchmarks

Intended row unit: one simulated benchmark run for one software test case and
version. File: `deployment_benchmarks.csv`, UTF-8, comma-separated, header
present. It has 280 rows and no missing fields. The `independent` cohort uses
different case IDs for the two versions; the `paired` cohort measures each case
under both versions. Select the design before selecting a test.

| Variable | Meaning | Statistical type | Units / valid values |
| --- | --- | --- | --- |
| `design` | Comparison cohort design | Nominal categorical | `independent`, `paired` |
| `case_id` | Test-case identifier | Nominal identifier | `I-001`/`J-001` for separate independent cases; shared `P-001`–`P-060` within pairs |
| `version` | Software version condition | Nominal categorical | `baseline`, `optimized`; not randomized in a real deployment |
| `loc` | Simulated source lines of code for a case | Numerical, conceptually continuous | Lines; repeated across the two rows of each paired case |
| `cyclomatic_complexity` | Simulated case complexity metric | Numerical, discrete | Nonnegative integer metric |
| `response_time_ms` | Simulated run response time | Numerical, conceptually continuous | Milliseconds |
| `passed` | Simulated test outcome | Binary categorical | `True`, `False` |

This is a constructed scenario, not observational production data. The
independent and paired cohorts are simulated separately; do not pool them into
one comparison. The generated version differences are teaching inputs, not
causal evidence. LOC and complexity are associated by construction and do not
establish why a run is slower or whether a change is beneficial in practice.
