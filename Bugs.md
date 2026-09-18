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
User: (space) pinkudoe@gmail.com
Password: Prueba12345!

## Expected Result
System handles the spaces according to the specified requirements 

## Actual Result
The system allows the user to access the account despite the incorrect password.

## Evidence
<img width="750" height="608" alt="image" src="https://github.com/user-attachments/assets/7f52f613-bd84-4b18-aaf2-649f7bb126d8" />

## Related Test Case
TC-008

## Status
Open
