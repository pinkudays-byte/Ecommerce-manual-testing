# Test Cases 

## 1. Authentication


# ID: TEC-001 
## Over this test I will use a Positive Testing following the "happy Path". 
- Test case: Verify a user with valid email and correct password can successfully log in and is redirected to the
 home/dashboard page.
- Preconditions: Registered user
- Steps:
  - Enter in Sign In
  - Enter in Sigh Account 
  - Register valid information on the dashboard 
  - Click in register
- Test data: Valid Information on the dashboard "Costumer registration" 
- Expected result: Registration success 
- Actual result:
- Status:

# ID: TEC-002 
## Boundary Value Analysis, looking for a test beyond the happy path 
- Test case: Registration (Boundary Value Analysis): Test with weak vs. strong passwords, already registered email, and invalid email formats.
- Preconditions: Use a wrong over a user already registered. 
- Steps:
  -Enter in to "long in" 
  -Fill the camp with a valid user 
  -Fill the camp with a invalid password
- Test data:
  -User: Pinku@gmail.com
  -Password: 123456789 
- Expected result: The system should show an appropriate error message
- Actual result: 
- Status:
