# Workforce KPI Definitions

This reference defines the intended calculations for the HR analytics practice project. Confirm the exact source columns and population before implementing these definitions in SQL, Python, or Power BI.

## Core metrics

| Metric | Definition | Validation note |
|---|---|---|
| Headcount | Count of distinct employee IDs in the selected population | Confirm one row per employee or deduplicate using a documented rule |
| Attrition Count | Count of distinct employees whose attrition status indicates they left | Validate allowed status values and missing labels |
| Attrition Rate | Attrition count divided by the eligible employee population | State exclusions and denominator explicitly |
| Average Monthly Income | Mean monthly income for employees with a valid income value | Report the non-missing sample size |
| Average Tenure | Mean tenure for employees with a valid tenure value | Confirm unit (months or years) |

## Comparison rules

- Show group sizes beside department, role, and other segment rates.
- Use the same eligibility rules when comparing groups.
- Do not compare averages calculated from different or undocumented populations.
- Report missing values rather than silently treating them as zero.
- Validate date ordering and numeric ranges before calculating derived metrics.

## Interpretation and limitations

- Segment differences are descriptive associations; they do not establish causation.
- Do not use these practice analyses to rank individual employees or make employment decisions.
- Identify whether the dataset is synthetic or otherwise illustrative before publishing findings.
- Add numerical results only after reproducing them from the current repository data and code.

## Implementation checklist

- [ ] Confirm the dataset grain and employee key.
- [ ] Confirm the attrition status values and eligible population.
- [ ] Validate missingness and category labels.
- [ ] Reconcile total headcount and attrition count to source records.
- [ ] Verify segment denominators and display sample sizes.
- [ ] Re-run calculations after data refresh.
