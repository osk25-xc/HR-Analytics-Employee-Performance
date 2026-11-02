# HR Dataset Validation Guide

## Structure
Establish whether the file is a current employee snapshot or a historical employee-event table. Confirm the expected key and duplicate policy.

## Field checks
Validate department and role categories, hire and exit dates, numeric compensation fields, satisfaction scale bounds, and missing performance labels. Flag impossible date sequences for review rather than silently deleting rows.

## Metric definitions
Document the eligible population and period for attrition rate. Calculate compensation summaries with units and currency clearly stated. Show group counts with averages and rates.

## Fairness and privacy
Avoid publishing employee-level personal details. Small groups may expose identities; suppress or combine them where appropriate. Group patterns are not a sufficient basis for individual employment decisions.
