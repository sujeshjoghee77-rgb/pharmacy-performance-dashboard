# Healthcare Data Governance

## Purpose
Demonstrate responsible handling of a fabricated synthetic healthcare dataset for educational purposes only.

## Field classification
- `patient_id`: pseudonymous identifier. It is not a direct identifier, but linkage risk depends on how it was generated and whether a re-identification key exists.
- `age_years`, `sex`, `visit_date`, `postal_code`: demographic or quasi-identifying fields. In combination, these may increase re-identification risk.
- `systolic_bp_mmHg`, `diastolic_bp_mmHg`, `diagnosis`: sensitive clinical data.
- `department`: operational/administrative data.

## De-identification assessment
The demo has no names, phone numbers, email addresses, or street addresses. Patient IDs are synthetic labels. However, removing direct identifiers alone does not guarantee de-identification. Dates, age, sex, and postal area can become identifying when combined. A formal assessment and access controls are required before any real-world release.

## Safe handling
- Preserve the raw file.
- Work on a copy.
- Minimise fields to those required.
- Do not upload real patient data to a public repository.
- Do not infer missing clinical values.
- Keep an exception log for unresolved issues.

## Validation and cleaning
Whitespace is trimmed, blank strings become missing, dates are parsed, and invalid dates are flagged. Repeated IDs and duplicate rows are flagged rather than removed. No clinical range checks are applied because no approved clinical reference limits were provided.

## Limitations
This is a demonstration schema, not an official clinical data dictionary. Replace it with the supplied task materials if they become available.
