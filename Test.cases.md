# Test Cases 

## 1. 



# Test Cases - Login 

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

# Test Cases - Product management

| ID | Test Case | Preconditions | Steps | Test Data | Technique | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|---|---|
| TC-014 | View product details | Product catalog is available | Select a product from the product listing | Available product | Equivalence Partitioning | The product details page is displayed with the corresponding product information | — | Not Run |
| TC-015 | Verify product information consistency | Product details page is available | Compare product name, image, price, and availability between the product listing and product details page | Available product | Error Guessing | Product information is consistent between the product listing and product details page | — | Not Run |
| TC-016 | Add a product to the cart | Product is available | Open product details → Click **Add to Cart** | Available product | Equivalence Partitioning | The selected product is successfully added to the cart and the cart is updated accordingly | — | Not Run |
| TC-017 | Add multiple quantities of a product to the cart | Product is available and quantity selector is enabled | Select a quantity → Click **Add to Cart** | Quantity: 2 | Equivalence Partitioning | The selected quantity is added to the cart and the total quantity is displayed correctly | — | Not Run |
| TC-018 | Add maximum allowed quantity to the cart | Product has a defined maximum quantity | Select the maximum allowed quantity → Click **Add to Cart** | Maximum allowed quantity | Boundary Value Analysis | The system allows the maximum permitted quantity to be added to the cart | — | Not Run |
| TC-019 | Attempt to exceed maximum product quantity | Product has a defined maximum quantity | Select a quantity above the maximum allowed → Click **Add to Cart** | Maximum allowed quantity + 1 | Boundary Value Analysis | The system prevents the user from exceeding the maximum allowed quantity and displays an appropriate message | — | Not Run |
| TC-020 | Add product to Favorites | User is logged in and product is available | Open product details → Click **Add to Favorites** | Available product | State Transition Testing | The product is added to the user's Favorites list | — | Not Run |
| TC-021 | Remove product from Favorites | User is logged in and product is already in Favorites | Open product details → Click **Remove from Favorites** | Favorited product | State Transition Testing | The product is removed from the user's Favorites list | — | Not Run |
| TC-022 | Verify Favorites persistence after logout | User is logged in and has products in Favorites | Add product to Favorites → Logout → Login again → Open Favorites | Favorited product | State Transition Testing | The previously favorited product remains in the user's Favorites list after logging in again | — | Not Run |
| TC-023 | Add product to Favorites while browsing | User is logged in and product catalog is available | Click the Favorites icon on a product card | Available product | State Transition Testing | The selected product is added to Favorites without requiring the user to open the product details page | — | Not Run |
| TC-024 | Navigate between product listing and product details | Product catalog is available | Select a product → Return to product listing → Select another product | Two available products | State Transition Testing | The user can navigate between product listing and product details without losing the selected product information | — | Not Run |
| TC-025 | Verify cart contents after continuing to browse | Product is available | Add product to cart → Return to product listing → Open another product | Available products | State Transition Testing | The previously added product remains in the cart while the user continues browsing | — | Not Run |
| TC-026 | Verify related products | Product details page is available | Open a product → Scroll to **Related Products** | Available product | Equivalence Partitioning | Related products are displayed according to the product category or defined requirements | — | Not Run |

# Test Cases - Product Discovery

| ID | Test Case | Preconditions | Steps | Test Data | Technique | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|---|---|
| TC-027 | Sort products by price Low to High | Product catalog is available | Open the **Sort** dropdown → Select **Price Low to High** | Price Low to High | Equivalence Partitioning | Products are displayed in ascending order based on price | — | Not Run |
| TC-028 | Sort products by price High to Low | Product catalog is available | Open the **Sort** dropdown → Select **Price High to Low** | Price High to Low | Equivalence Partitioning | Products are displayed in descending order based on price | — | Not Run |
| TC-029 | Filter products by category | Product catalog is available | Select a category under **By category** | Hammer | Equivalence Partitioning | Only products belonging to the selected category are displayed | — | Not Run |
| TC-030 | Filter products by multiple categories | Product catalog is available | Select multiple categories under **By category** | Hammer + Hand Saw | Equivalence Partitioning | The displayed products match the selected category criteria according to the system requirements | — | Not Run |
| TC-031 | Filter products by brand | Product catalog is available | Select a brand under **By brand** | Brand name 1 | Equivalence Partitioning | Only products belonging to the selected brand are displayed | — | Not Run |
| TC-032 | Filter products by multiple brands | Product catalog is available | Select multiple brands under **By brand** | Brand name 1 + Brand name 2 | Equivalence Partitioning | The displayed products match the selected brand criteria according to the system requirements | — | Not Run |
| TC-033 | Filter products by price range | Product catalog is available | Adjust the minimum and maximum values on the **Price Range** slider | Minimum: 50 / Maximum: 150 | Boundary Value Analysis | Only products within the selected price range are displayed | — | Not Run |
| TC-034 | Filter products using minimum price boundary | Product catalog is available | Set the minimum price to the lowest available value → Apply filter | Minimum price: 1 | Boundary Value Analysis | Products at or above the minimum selected price are displayed | — | Not Run |
| TC-035 | Filter products using maximum price boundary | Product catalog is available | Set the maximum price to the highest available value → Apply filter | Maximum price: 200 | Boundary Value Analysis | Products at or below the maximum selected price are displayed | — | Not Run |
| TC-036 | Filter products by category and brand | Product catalog is available | Select a category → Select a brand | Category: Hammer + Brand: Brand name 1 | Decision Table Testing | Only products satisfying the selected category and brand criteria are displayed | — | Not Run |
| TC-037 | Filter products by category, brand, and price range | Product catalog is available | Select category → Select brand → Set price range | Hammer + Brand name 1 + $50–$150 | Decision Table Testing | Only products matching all selected filter criteria are displayed | — | Not Run |
| TC-038 | Filter products by sustainability | Product catalog is available | Select **Show only eco-friendly products** | Sustainability: Enabled | Equivalence Partitioning | Only products identified as eco-friendly/sustainable are displayed | — | Not Run |
| TC-039 | Combine sustainability with other filters | Product catalog is available | Select category → Select brand → Enable sustainability filter | Hammer + Brand name 1 + Eco-friendly | Decision Table Testing | Only products matching all selected criteria are displayed | — | Not Run |
| TC-040 | Clear individual filter | At least one filter is applied | Apply a filter → Remove the selected filter | Category: Hammer | State Transition Testing | The selected filter is removed and the product results are updated accordingly | — | Not Run |
| TC-041 | Clear all applied filters | Multiple filters are applied | Apply category, brand, price, and sustainability filters → Clear all filters | Multiple active filters | State Transition Testing | All filters are reset and the default product results are displayed | — | Not Run |
| TC-042 | Search for an exact product | Product catalog is available | Enter a product name in the **Search** field → Click **Search** | Hammer | Error Guessing | The system displays the product matching the search term | — | Not Run |
| TC-043 | Search using a partial product name | Product catalog is available | Enter part of a product name → Click **Search** | Hamm | Error Guessing | The system displays products relevant to the partial search term | — | Not Run |
| TC-044 | Search for a non-existent product | Product catalog is available | Enter a product name that does not exist → Click **Search** | `NonexistentProduct123` | Error Guessing | The system displays an appropriate message indicating that no matching products were found | — | Not Run |
| TC-045 | Search with special characters | Product catalog is available | Enter special characters in the search field → Click **Search** | `@#$%` | Error Guessing | The system handles the input appropriately without errors or unexpected behavior | — | Not Run |
| TC-046 | Apply filters after performing a search | Search results are displayed | Search for a product → Apply category or brand filter | Search: Hammer + Category: Hand Tools | Decision Table Testing | The displayed results satisfy both the search criteria and the selected filter | — | Not Run |
| TC-047 | Sort filtered results | Products are filtered | Apply a category or brand filter → Select a sorting option | Category: Hand Tools + Price Low to High | Decision Table Testing | Filtered products remain displayed and are sorted according to the selected sorting option | — | Not Run |

# Test Cases - Checkout

| ID | Test Case | Preconditions | Steps | Test Data | Technique | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|---|---|---|
| TC-048 | Update product quantity in the cart | Cart contains a product | Increase the product quantity → Update cart | Quantity: 2 | Boundary Value Analysis | The product quantity and cart total are updated correctly | — | Not Run |
| TC-049 | Remove a product from the cart | Cart contains at least one product | Click **Remove** for a product | Product in cart | State Transition Testing | The selected product is removed and the cart total is updated accordingly | — | Not Run |
| TC-050 | Proceed to checkout with a product in the cart | Cart contains at least one product | Open Cart → Click **Checkout** | Product in cart | Equivalence Partitioning | The system proceeds to the checkout process | — | Not Run |
| TC-051 | Sign in during checkout with valid credentials | User is not signed in and has a product in the cart | Proceed to checkout → Enter username and password → Sign In | Valid username + valid password | Equivalence Partitioning | User is successfully authenticated and proceeds to the next checkout step | — | Not Run |
| TC-052 | Sign in during checkout with invalid credentials | User is not signed in and has a product in the cart | Proceed to checkout → Enter invalid credentials → Sign In | Valid username + incorrect password | Equivalence Partitioning | Sign in is rejected and an appropriate error message is displayed | — | Not Run |
| TC-053 | Attempt to proceed without signing in | User is not signed in and has a product in the cart | Proceed to checkout without providing credentials | Empty username + empty password | Equivalence Partitioning | The system prevents the user from proceeding and displays appropriate validation messages | — | Not Run |
| TC-054 | Complete checkout with valid payment information | User is signed in and has reached the payment step | Enter required payment information → Continue | Valid test payment data | Equivalence Partitioning | Payment information is accepted and the user proceeds to order review | — | Not Run |
| TC-055 | Submit payment with required fields empty | User is signed in and is on the payment step | Leave required payment fields empty → Continue | Empty required fields | Equivalence Partitioning | The system prevents the user from proceeding and displays appropriate validation messages | — | Not Run |
| TC-056 | Submit invalid payment information | User is signed in and is on the payment step | Enter invalid payment information → Continue | Invalid test payment data | Equivalence Partitioning | The system rejects the payment information and displays an appropriate error message | — | Not Run |
| TC-057 | Enter payment information at minimum allowed limits | User is signed in and is on the payment step | Enter values at the minimum allowed limits → Continue | Minimum valid test values | Boundary Value Analysis | The system accepts values that meet the minimum requirements | — | Not Run |
| TC-058 | Review order before placing the order | User has completed the checkout steps | Review products, quantities, payment information, and total | Selected product(s) + valid test payment | Equivalence Partitioning | Order information is displayed correctly before the order is submitted | — | Not Run |
| TC-061 | Complete purchase with valid information | User is signed in and has completed the required checkout information | Review order → Click **Place Order** | Valid product(s) + valid test payment | End-to-End Testing | The order is successfully placed and an appropriate order confirmation is displayed | — | Not Run |
| TC-062 | Verify cart after successful purchase | User has successfully completed an order | Complete purchase → Return to cart | Purchased product(s) | State Transition Testing | The cart is updated according to the defined requirements after the purchase is completed | — | Not Run |
