# Lab 5 – Static Code Analysis Reflection

## 1. What is static code analysis, and why is it useful?

Static code analysis examines source code without executing it. It helps identify potential bugs, security vulnerabilities, and coding-style problems early in development. This makes code easier to maintain and reduces the chance of errors.

## 2. What did Pylint, Bandit, and Flake8 help identify?

- **Pylint:** Helped identify code-quality issues, including import-order problems and the use of a global statement.
- **Bandit:** Helped identify security-sensitive coding patterns, including insecure file-transfer and command-execution approaches.
- **Flake8:** Identified formatting issues such as excessive blank lines, whitespace problems, and lines exceeding the permitted length.

## 3. What improvements were made to the program?

I corrected the EMI interest-rate calculation, replaced the mutable default argument with a safer approach, validated loan types and application data, improved file handling, replaced insecure FTP transfer with SFTP, and improved application ID generation. I also corrected formatting and import-order issues.

## 4. What did I learn from this lab?

I learned that different static analysis tools focus on different aspects of a program. Using them together helps improve code quality, readability, maintainability, and security. I also learned that after changing code, I should rerun the tools and test the program to verify the changes.

## 5. What are the limitations of static analysis?

Static analysis can identify many potential problems, but it cannot guarantee that a program is completely secure or logically correct. Some issues require runtime testing, code review, and tests with different inputs. Security findings should therefore be reviewed rather than blindly ignored or suppressed.

## Final Verification

- Pylint score: 9.79/10
- Flake8: No issues reported
- Bandit: 0 High, 0 Medium, 0 Low findings in the latest report
- Program execution: Completed successfully
