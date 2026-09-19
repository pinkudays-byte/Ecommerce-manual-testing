# BUG-001 — The system does not handle spaces in the username field when attempting to log in.

## Summary
The system did not recognize spaces correctly

## Severity
Medium

## Priority
Low

## Environment
- Browser: Firefox
- Browser version: 155
- Operating System: Windows 11

## Preconditions
- Use a user and valid password

## Steps to Reproduce

1.- Insert at least one space in the user label
2.- Insert a valid Password
3.- Click in login 

## Test Data
- User: (space) pinkudoe@gmail.com
- Password: Prueba12345!

## Expected Result
System handles the spaces according to the specified requirements 

## Actual Result
The system output a error message besides the user and password is correct 

## Evidence
<img width="750" height="608" alt="image" src="https://github.com/user-attachments/assets/7f52f613-bd84-4b18-aaf2-649f7bb126d8" />

## Related Test Case
TC-008

## Status
Open


# BUG-002 — Login with uppercase email

## Summary
- The system did not recognize uppercase in the user label 

## Severity
- High

## Priority
- High

## Environment
- Browser: Firefox
- Browser version: 155
- Operating System: Windows 11

## Preconditions
- Use a user and valid password

## Steps to Reproduce

1.- Insert a valid user with uppercase 
2.- Insert a valid Password
3.- Click in login 

## Test Data
- PINKUDOE@GMAIL.COM

## Expected Result
- The system should recognize the uppercase and valid the data besides this format

## Actual Result
- The system did not recognize uppercase

## Evidence


## Related Test Case
TC-008

## Status
