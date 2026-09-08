# Test Cases 

## 1. 



# Login Test Cases

## Objective

Validate the login functionality by testing valid credentials, invalid inputs, boundary conditions, account states, and scenarios outside the happy path.

## Test Cases-Authentication
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
| TC-011 | Register with valid information | Registration page is available | Enter all required information → Click **Register** | First name: `John`<br>Last name: `Doe`<br>Address: `123 Main Street`<br>Postcode: `90210`<br>City: `Los Angeles`<br>State: `California`<br>Country: `United States`<br>Phone: `5551234567`<br>Email: `john.doe.test@example.com`<br>Password: `Test1234!` | Equivalence Partitioning | User account is successfully created and the system proceeds to the appropriate next step | — | Not Run |
| TC-012 | Test registration fields with minimum input values to identify required fields and minimum length restrictions  | User is on the registration page and the registration form is displayed | Enter minimum input values in all fields → Click Register | Valid email + correct password | Boundary Value Analysis | The system should display appropriate validation messages for required fields and inputs that do not meet the minimum length requirements. | — | Not Run |
