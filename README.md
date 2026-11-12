# Healthcare Data Governance and Cleaning

## Important disclosure
The task-page CSV and governance guide were not available to download. Therefore, this repository uses a **fabricated synthetic demonstration dataset** created only to show the requested workflow. It is not the original task-provided dataset and contains no real patient records.

## Objective
Demonstrate privacy-aware data classification, data-quality validation, conservative cleaning, and exception logging.

## Files
- `data/raw/synthetic_demo_patient_records.csv` — fabricated demo input with deliberate quality issues.
- `data/cleaned_patient_records.csv` — output after whitespace/blank/date-format cleaning; clinical values are not imputed.
- `data/data_dictionary.csv` — field descriptions and governance classification.
- `data/exception_log.csv` — missing values, date parse failure, duplicate row and repeated patient ID flags.
- `data/quality_profile.csv` — data-quality profile.
- `notebooks/healthcare_data_cleaning.ipynb` — reproducible notebook.
- `docs/data_governance.md` — governance and privacy notes.
- `docs/cleaning_report.md` — summary and limitations.

## Run
Install dependencies: `pip install pandas numpy jupyter`
Open `notebooks/healthcare_data_cleaning.ipynb` in Jupyter and run all cells.

## Rules
No clinical values are invented or imputed. No clinical ranges are asserted without an approved source. Duplicate IDs are flagged for review and not automatically deleted. Keep any actual patient data private and out of public repositories.
