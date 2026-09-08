# Test Cases 

## 1. 



# Login Test Cases

## Objective

Validate the login functionality by testing valid credentials, invalid inputs, boundary conditions, account states, and scenarios outside the happy path.

## Test Cases

| ID | Test Case | Preconditions | Steps | Test Data | Technique | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|---|---|
| TC-001 | Login with valid credentials | Registered user | Enter credentials → Login | Valid email/password | Equivalence Partitioning | User accesses account | — | Not Run |
| TC-002 | Login with incorrect password | Registered user | Enter valid email + wrong password → Login | Valid email + incorrect password | Equivalence Partitioning | Login is rejected | — | Not Run |
| TC-003 | Login with unregistered email | User is not registered | Enter unregistered email + password → Login | Unregistered email + valid-format password | Equivalence Partitioning | Login is rejected | — | Not Run |
| TC-004 | Login with empty email | Login page is available | Leave email empty → Enter password → Login | Empty email + valid password | Equivalence Partitioning | Login is rejected and an appropriate validation message is displayed | — | Not Run |
| TC-005 | Login with empty password | Login page is available | Enter email → Leave password empty → Login | Valid email + empty password | Equivalence Partitioning | Login is rejected and an appropriate validation message is displayed | — | Not Run |
| TC-006 | Login with both fields empty | Login page is available | Leave email and password empty → Login | Empty email + empty password | Equivalence Partitioning | Login is rejected and validation messages are displayed | — | Not Run |
| TC-007 | Login with invalid email format | Login page is available | Enter invalid email format + password → Login | `user@` + valid password | Equivalence Partitioning | Login is rejected and an appropriate validation message is displayed | — | Not Run |
| TC-008 | Login with leading/trailing spaces in email | Registered user | Enter email with spaces → Enter password → Login | ` test@example.com ` + valid password | Error Guessing | System handles the spaces according to the specified requirements | — | Not Run |
| TC-009 | Login with uppercase email | Registered user | Enter email using uppercase characters → Enter password → Login | `TEST@EXAMPLE.COM` + valid password | Error Guessing | System handles the email according to the specified requirements | — | Not Run |
| TC-010 | Login after multiple failed attempts | Registered user with defined failed-attempt policy | Enter incorrect password repeatedly → Login | Valid email + incorrect password | Boundary Value Analysis | System applies the defined failed-attempt policy | — | Not Run |
| TC-011 | Login after account lockout threshold | Registered user with defined lockout policy | Exceed maximum failed attempts → Login | Valid email + incorrect password | Boundary Value Analysis | Account is locked according to the defined requirements | — | Not Run |
| TC-012 | Login after account is locked | Account has been locked | Enter correct credentials → Login | Valid email + correct password | State Transition Testing | System handles the locked account according to the defined requirements | — | Not Run |
