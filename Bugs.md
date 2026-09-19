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
The system displays an error message even though the username and password are correct.

## Evidence
<img width="750" height="608" alt="image" src="https://github.com/user-attachments/assets/7f52f613-bd84-4b18-aaf2-649f7bb126d8" />

## Related Test Case
TC-008

## Status
Open






# BUG-002 —  	Add a product to the cart

## Summary
- The system displays an error message even though the function is working correctly.

## Severity
- Medium

## Priority
- High

## Environment
- Browser: Firefox
- Browser version: 155
- Operating System: Windows 11

## Preconditions
- The product and cart stage should be available 

## Steps to Reproduce
- Click a product
- Verify if the product was added correctly

## Test Data
- Product: Combination Pliers

## Expected Result
- The product should added in the car 

## Actual Result
- The product is successfully added, but an error message is displayed.

## Evidence
<img width="1557" height="480" alt="image" src="https://github.com/user-attachments/assets/b0f7ad96-1a88-4483-876c-609489be380f" />
<img width="1240" height="361" alt="image" src="https://github.com/user-attachments/assets/3c1ce446-88b8-4ce0-b95f-664f03ad7367" />


## Related Test Case
TC-016

## Status
Open
