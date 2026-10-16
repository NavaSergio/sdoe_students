# Formative assessment — Session 02

Revision ID: S02-r1

## Learning outcomes assessed

1. Select records and derive a variable while preserving raw data.
2. Justify separate treatments of duplicates, missing values, and invalid values.
3. Report group summaries with record and observed-value counts.
4. Communicate units, missingness, and limits of a descriptive comparison.

## Instructions and grading criteria

Use the notebook and data dictionary. Work individually during the last ten
minutes: Q1–Q3 in seven minutes and Q4 in three. Submit responses with IDs.
Ten feedback points, no final-grade weight: eight for reasoning, two for code.
Use units, justify decisions, and identify the relevant denominator. Partial
credit recognizes correct reasoning even when code needs a small correction.

## S02-Q1

Points: 3

A closed incident has resolution_hours = -4; another has no recorded duration; an entire export row appears twice. Describe a defensible treatment for each and explain why replacing all three issues with zero is inappropriate.

Your response:

____________________

## S02-Q2

Points: 3

A cleaned service group has records = 7, observed = 4, and mean_hours = 8. State the denominator of the mean, the number of missing durations, and one limitation when comparing this mean with another service.

Your response:

____________________

## S02-Q3

Points: 2

Given a cleaned DataFrame clean, select service == "api" into api_only and create resolution_days by dividing resolution_hours by 24. Preserve clean unchanged.

Your response:

____________________

## S02-Q4

Points: 2

A version has a lower observed mean duration. Give one reason this does not establish a causal improvement, and name one additional piece of information you would request.

Your response:

____________________
