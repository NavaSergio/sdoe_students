# Cumulative practical task — Sessions 01–04

Student version — public

Revision ID: S04-r1

## Instructions and grading criteria

Use the Session 04 notebook, the data dictionary, and the cleaned DataFrame `clean` produced with the Session 02 policy. Work individually and submit responses or code under each question ID. The task is worth 10 points for criterion-based feedback; any course-grade weighting will be announced separately. Q1 is worth 2 points, Q2 3, Q3 2, and Q4 3. At least half the points assess reasoning and interpretation. Use variable names, units, and observed counts. Do not treat missing values as zero, an unusual value as an automatic error, or an exploratory pattern as causal evidence.

Use only pandas and matplotlib concepts from the course. The data are the synthetic software-incident export embedded in the Session 04 notebook; no external download or additional package is needed.

## Learning outcomes assessed

1. Identify the observational unit, available records, and conceptual variable types.
2. Explain and apply the documented handling of duplicates, missing values, and invalid durations.
3. Calculate and interpret center and spread with units and denominators.
4. Choose, label, and interpret exploratory plots without overstating what the data show.

## S04-Q1

Points: 2

For this export, state what one observational unit represents and how many distinct incidents remain after exact duplicate handling. Classify `incident_id`, `service`, `severity`, and `resolution_hours` as categorical or numerical; identify which is an identifier and which is an ordered category. Include the unit for `resolution_hours`.

Your response:

____________________

## S04-Q2

Points: 3

Apply the Session 02 cleaning policy. In a cleaned DataFrame `clean`, report the number of distinct incident records and observed `resolution_hours` values. Explain how the exact repeated row, negative duration, and missing service are handled. Then write code to show incident-record counts and observed-duration counts by `service`.

Your response or code:

____________________

## S04-Q3

Points: 2

Using the nonmissing `resolution_hours` values in `clean`, calculate the mean, median, Q1, Q3, and IQR in hours. State which center you would use to describe a typical observed duration and briefly justify your choice using the results or distribution.

Your response or code:

____________________

## S04-Q4

Points: 3

Create (a) a histogram of the observed `resolution_hours` values and (b) a boxplot of observed resolution hours by service with the individual observations visible. Label axes and units, report the relevant observed counts, and state one pattern and one limitation. Do not use `incident_id` as time or claim that a group difference is causal.

Your response or code:

____________________
