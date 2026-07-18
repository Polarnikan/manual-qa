|ID|Title|Priority|Status|
|SD-TC-001|Successful Login in|High|Passed|
Environment: Opera GX 133 (Chromium-based), Windows 11
Preconditions: User is on the login-in page (https://www.saucedemo.com); standard_user account is active

Test Data:
user: standard_user 
password: secret_sauce

steps:
1-Open Login Page
2-Insert Valid Username
3-Insert Valid Password
4-Press "Login" button

Expectation Results:
User Successfully logins and redirected to catalogue (/inventory.html)

Actual Result:User successfully redirected to catalogue

Status: Passed
