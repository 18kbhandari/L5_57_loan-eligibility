# Lab 5 – Static Code Analysis Issues

## 1. Overview

The original `loan_calculator.py` was analysed using Pylint, Bandit, and Flake8 before making any changes.

**Initial Pylint score:** 5.17/10

## 2. Issues Identified

| No. | Issue | Tool / Category | Planned Fix |
|---|---|---|---|
| 1 | Unused imports | Pylint / Flake8 | Remove imports that are not required. |
| 2 | Mutable default argument in `checkEligibility()` | Code quality | Use `None` as the default and create a new list inside the function. |
| 3 | Incorrect annual interest-rate conversion in EMI calculation | Logic error | Convert the annual percentage rate to a monthly decimal rate consistently. |
| 4 | Eligibility checks can approve invalid loan applications | Logic error | Validate the loan type and apply eligibility checks in a consistent order. |
| 5 | Use of `sum` as a variable name | Code quality | Rename the variable to avoid shadowing Python's built-in `sum()` function. |
| 6 | Insecure use of `marshal` to load saved data | Security | Replace it with a safer data-storage format, such as JSON, and validate loaded data. |
| 7 | Hardcoded FTP credentials | Security | Read credentials from environment variables instead of storing them in source code. |
| 8 | FTP connection does not encrypt transferred data | Security | Use a secure transfer method, such as SFTP or properly configured FTPS. |
| 9 | Files are opened without context managers | Code quality / Reliability | Use `with open(...)` so files are closed automatically. |
| 10 | Application IDs use the `random` module | Security / Reliability | Use a more suitable unique-ID generation method. |

## 3. Expected Improvements

- Improve the Pylint score.
- Reduce code-style and formatting warnings.
- Address security weaknesses identified by Bandit.
- Correct loan calculation and eligibility logic.
- Improve file handling and maintainability.

*Note: The final issue list and severity levels should be checked against the saved Pylint, Bandit, and Flake8 reports.*
