|ID|Title|Priority|Status|
|---|---|---|---|
|SD-TC-001 |Successful Login in|High|Passed|
|SD-TC-002 |Login in with invalid Username|Medium|Passed|
|SD-TC-003 |Login in with invalid Password|Medium|Passed|
|SD-TC-004 |Adding single product to cart qty=1|High|Passed| 
|SD-TC-005 |Adding single product to cart qty>1|High|Blocked| 


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
