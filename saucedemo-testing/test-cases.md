|ID|Title|Priority|Status|
|---|---|---|---|
|SD-TC-001 |Successful Login in|High|Passed|

**Environment**: Opera GX 133 (Chromium-based), Windows 11

**Preconditions**: User is on the login-in page (https://www.saucedemo.com); standard_user account is active

**Test Data**:
- user: standard_user
- password: secret_sauce

**Steps:**
1. Open Login Page
2. Insert Valid Username
3. Insert Valid Password
4. Press "Login" button

**Expectation Results**: User Successfully logins and redirected to catalogue (/inventory.html)

**Actual Result**: User successfully redirected to catalogue

**Status**: Passed


|ID|Title|Priority|Status|
|---|---|---|---|
|SD-TC-002 |Invalid Username|Medium|Passed|

**Environment**: Opera GX 133 (Chromium-based), Windows 11

**Preconditions**: User is on the login-in page (https://www.saucedemo.com); standard_user account is active

**Test Data**:
- user: standard_user
- password: secret_sauce

**Steps:**
1. Open Login Page
2. Insert Invalid Username
3. Insert Valid Password
4. Press "Login" button

**Expectation Results**: System displays an error message indicating invalid credentials.  

**Actual Result**: System displays generic error message: "Epic sadface: Username and password do not match any user in this service" (same message shown regardless of whether username or password was incorrect — see UX-001)

**Status**: Passed

|ID|Title|Priority|Status|
|---|---|---|---|
|SD-TC-003 |Invalid Password|Medium|Passed|

**Environment**: Opera GX 133 (Chromium-based), Windows 11

**Preconditions**: User is on the login-in page (https://www.saucedemo.com); standard_user account is active

**Test Data**:
- user: standard_user
- password: secret_sauce

**Steps:**
1. Open Login Page
2. Insert Valid Username
3. Insert Invalid Password
4. Press "Login" button

**Expectation Results**: System displays an error message indicating invalid credentials.  

**Actual Result**: System displays generic error message: "Epic sadface: Username and password do not match any user in this service" (same message shown regardless of whether username or password was incorrect — see UX-001)

**Status**: Passed
