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

# BUG-002 —  Login with uppercase email

## Summary
- The system does not recognize uppercase letters in the username field.

## Severity
- High

## Priority
- High

## Environment
- Browser: Firefox
- Browser version: 155
- Operating System: Windows 11

## Preconditions
- User a valid user and password

## Steps to Reproduce
- Use a user with a at least one upper case letter 

## Test Data
- User: PINKUDOE@GMAIL.COM 
- Password: Prueba12345!

## Expected Result
- The system should accept uppercase and lowercase letters and validate the username based on its format.

## Actual Result
- The system does not recognize uppercase letters even though the username is valid.

## Evidence
<img width="895" height="496" alt="image" src="https://github.com/user-attachments/assets/cc5e7c7f-c7eb-4371-b5bf-ec5c2bf008d9" />


## Related Test Case
TC-009

## Status
Open


# BUG-003 —  	Add a product to the cart

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

# BUG-004 —  	Add multiple quantities of a product to the cart

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
- Click on at least a 2 product
- Verify if the product was added correctly

## Test Data
- Product: Combination Pliers
- Product: Pliers 

## Expected Result
- The products should added in the car 

## Actual Result
- The products is successfully added, but an error message is displayed.

## Evidence
<img width="1606" height="454" alt="image" src="https://github.com/user-attachments/assets/06ce8b3d-a6ae-4746-92bb-6c529c6cdb91" />

## Related Test Case
TC-017

## Status
Open


# BUG-005 —  	Add product to Favorites

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
- Login
- Add a product to favorites 

## Steps to Reproduce
- Add a product to favorites
- Verify if the product was added correctly

## Test Data
- Product: Combination Pliers

## Expected Result
- The product is added to the user's Favorites list

## Actual Result
- The products is successfully added, but an error message is displayed.

## Evidence
<img width="1589" height="332" alt="image" src="https://github.com/user-attachments/assets/b07b35b7-d014-4210-983f-e02f016c762a" />


## Related Test Case
TC-020

## Status
Open


# BUG-006 — Sort products by price Low to High

## Summary
- The sort funtion is not working

## Severity
- High

## Priority
- High

## Environment
- Browser: Firefox
- Browser version: 155
- Operating System: Windows 11

## Preconditions
- The display of product should be available 

## Steps to Reproduce
- Choose a price with the function sort and click search 

## Test Data
- Sort for "1-55" 

## Expected Result
- The products should be sorted according to the selected criteria.  

## Actual Result
- The function is not working. The products do not change after selecting a sorting option.

## Evidence
<img width="1329" height="697" alt="image" src="https://github.com/user-attachments/assets/a631f2c5-55b2-4565-acfd-24a6f3449bd2" />

## Related Test Case
- TC-027

## Status
Open

# BUG-007 — Sort products by price high to low

## Summary
- The sort function is not working

## Severity
- High

## Priority
- High

## Environment
- Browser: Firefox
- Browser version: 155
- Operating System: Windows 11

## Preconditions
- The display of product should be available 

## Steps to Reproduce
- Choose a price with the function sort and click search 

## Test Data
- Sort for "55-200" 

## Expected Result
- The products should be sorted according to the selected criteria.  

## Actual Result
- The function is not working. The products do not change after selecting a sorting option.

## Evidence<img width="1342" height="743" alt="image" src="https://github.com/user-attachments/assets/9b97d08b-717d-4990-9fc8-63b25ebd60a3" />

## Related Test Case
- TC-028

## Status
Open










