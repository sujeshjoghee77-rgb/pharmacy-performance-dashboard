# Cleaning Report

## Dataset disclosure
This report uses a fabricated synthetic demonstration dataset because the task-page CSV and governance pack were not downloadable. It is not the original task dataset.

## Dataset profile
- Source rows: 14
- Columns: 9
- Missing cells in source: 3
- Rows involved in exact duplicates: 2
- Rows involved in repeated patient IDs: 2
- Unparseable visit dates: 1

## Field governance
See `data/data_dictionary.csv` and `docs/data_governance.md`. The fields include a pseudonymous ID, quasi-identifiers, sensitive clinical measurements/diagnosis, and an operational department field.

## Cleaning performed
- Trimmed leading/trailing whitespace in text fields.
- Converted blank strings to missing values.
- Parsed visit dates; unparseable dates were set to missing in the cleaned copy and logged.
- Preserved missing clinical measurements.
- Flagged duplicate rows and repeated patient IDs for review; did not automatically delete them.

## Clinical safety
No clinical values were invented, imputed, or altered. No clinical range validation was claimed because no approved reference range and units specification was supplied. Numeric summaries are descriptive only.

## Outstanding review
- Confirm whether repeated patient IDs represent valid multiple encounters or duplicates.
- Verify missing values against the authorised source.
- Confirm the permitted date format and field definitions from the official governance pack.
- Replace this demo with the supplied CSV if it becomes available.

## Conclusion
The project demonstrates reproducible data profiling, privacy-aware field classification, conservative cleaning, and exception logging. It is a substitute demonstration and should be disclosed as such during submission.
