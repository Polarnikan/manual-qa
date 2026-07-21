|ID|Title|Priority|Status|
|---|---|---|---|
|SD-TC-001 |Successful Login in|High|Passed|
|SD-TC-002 |Login in with invalid Username|Medium|Passed|
|SD-TC-003 |Login in with invalid Password|Medium|Passed|
|SD-TC-004 |Adding single product to cart qty=1|High|Passed| 
|SD-TC-005 |Adding single product to cart qty>1|High|Blocked| 
|SD-TC-006 |Sorting by alphabet |Medium|Passed|
|SD-TC-007 |Sorting by price |Medium|Passed|
|SD-TC-008 |Checkout process|High|Passed|

## ID: SD-TC-001 "Successful Login in"

**Environment**: Opera GX 133 (Chromium-based), Windows 11

**Preconditions**: User is on the login-in page (https://www.saucedemo.com); standard_user account is active

**Test Data**:
- username: standard_user
- password: secret_sauce

**Steps:**
1. Open Login Page
2. Insert Valid Username
3. Insert Valid Password
4. Press "Login" button

**Expectation Results**: User Successfully logins and redirected to catalogue (/inventory.html)

**Actual Result**: User successfully redirected to catalogue

**Status**: Passed

## ID: SD-TC-002 "Login in with invalid Username"

**Environment**: Opera GX 133 (Chromium-based), Windows 11

**Preconditions**: User is on the login-in page (https://www.saucedemo.com); standard_user account is active

**Test Data**:
- username: not_user
- password: secret_sauce

**Steps:**
1. Open Login Page
2. Insert Invalid Username
3. Insert Valid Password
4. Press "Login" button

**Expectation Results**: System displays an error message indicating invalid credentials.  

**Actual Result**: System displays generic error message: "Epic sadface: Username and password do not match any user in this service" (same message shown regardless of whether username or password was incorrect — see UX-001)

**Status**: Passed

## ID: SD-TC-003 "Login in with invalid Password"


**Environment**: Opera GX 133 (Chromium-based), Windows 11

**Preconditions**: User is on the login-in page (https://www.saucedemo.com); standard_user account is active

**Test Data**:
- username: standard_user
- password: secret_not

**Steps:**
1. Open Login Page
2. Insert Valid Username
3. Insert Invalid Password
4. Press "Login" button

**Expectation Results**: System displays an error message indicating invalid credentials.  

**Actual Result**: System displays generic error message: "Epic sadface: Username and password do not match any user in this service" (same message shown regardless of whether username or password was incorrect — see UX-001)

**Status**: Passed

## ID: SD-TC-004 "Adding single product to cart qty=1"

**Environment**: Opera GX 133 (Chromium-based), Windows 11

**Preconditions**: User is on the catalogue page (https://www.saucedemo.com/inventory.html); standard_user account is active

**Test Data**:
- None

**Steps** 
1. Open catalogue page
2. Press "add to cart" button for "Sauce labs Backpack" 
3. Press button with cart image.

**Expectation Results**: System add a product to users cart and displays added products with proper QTY and descriptions.  

**Actual results**:  System add a product to users cart and displays added products with proper QTY and descriptions.  

**Notes**: Cart view does not display image, only text. (name, discription,qty). See ENH-001 for improvment suggestion. 

**Status**: Passed 

## ID: SD-TC-005 "Adding single product to cart qty>1"

**Environment**: Opera GX 133 (Chromium-based), Windows 11

**Preconditions**: User is on the catalogue page (https://www.saucedemo.com/inventory.html); standard_user account is active

**Test Data**:
- None

**Steps** 
1. Open catalogue page
2. Press "add to cart" button for "Sauce labs Backpack" and choose qty/press button couple 3 more times
3. Press button with cart image.

**Expectation Results**: System add a product to users cart and ask for quanty of the item. Cart page displays added products with proper QTY and descriptions. 

**Actual results**: There is no mechanism to choose nor add more of a same item. After interaction "Add to cart" button changes to "Remove". No further possibility appeared. 

**Status**: Blocked/Not possible-function does not exist. 

## ID: SD-TC-006 "Sorting by alphabet "

**Environment**: Opera GX 133 (Chromium-based), Windows 11

**Preconditions**: User is on the catalogue page (https://www.saucedemo.com/inventory.html); standard_user account is active

**Test Data**:
- None

**Steps** 
1. Open catalogue page
2. Press "Filter" button and choose A-Z sorting
3. Press "Filter" button and choose Z-A sorting

**Expectation Results**: Page displays items assorted by name with a-z/z-a order

**Actual results**: Page displays items assorted by name with a-z/z-a order

**Status**: Passed

## ID: SD-TC-007 "Sorting by price"

**Environment**: Opera GX 133 (Chromium-based), Windows 11

**Preconditions**: User is on the catalogue page (https://www.saucedemo.com/inventory.html); standard_user account is active

**Test Data**:
- None

**Steps** 
1. Open catalogue page
2. Press "Filter" button and choose Low-High sorting
3. Press "Filter" button and choose High-Low sorting

**Expectation Results**: Page displays items assorted by name with Low-High/High-Low order

**Actual results**: Page displays items assorted by name with Low-High/High-Low order

**Status**: Passed

## ID: SD-TC-008 "Checkout Process"

**Environment**: Opera GX 133 (Chromium-based), Windows 11

**Preconditions**: User is on the cart page (https://www.saucedemo.com/cart.html) ; standard_user account is active

**Test Data**:
- "Sauce Labs Backpack"; "Sauce Labs Bolt T-Shirt"; "Sauce Labs Bicke Light"; in cart.
- Name/Surname: Jackson Gardan
- Zip/Postal Code: 89123

**Steps**:
1. Open cart page
2. Press Checkout
3. Input valid data (Name/surname/zipcode) (https://www.saucedemo.com/checkout-step-one.html)
4. Press "Continue" button
5. Press "Finish" Button at Overwiev page (https://www.saucedemo.com/checkout-step-two.html)
6. Press "Generate order PDF button" at "Checkout-comlete" page (https://www.saucedemo.com/checkout-complete.html)

**Expectation Results**: User is redirected from page to page step by step. Apon arrival to overview page user see tottal sum and list of items. After finishing payment page displays "Successful" and able to download PDF with order discriptions

**Actual results**: User is redirected from page to page step by step. List of items was valid and contained right sum. Payment and PDF downloaded downloaded.

**Status**: Passed
