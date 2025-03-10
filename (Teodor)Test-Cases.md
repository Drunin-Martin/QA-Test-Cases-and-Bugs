## Login // Logout // Registration
- **Target website:** https://teodor.bg/
## Test Case: Register with valid credentials
- **ID:** TC-018
- **Description:** Successfully create a new account
- **Preconditions:**
 - User does not have a profile in https://teodor.bg/
 - User has a a valid email address
- **Test Case Steps:**
1. Open website
2. Navigate to Login / Registration form
3. Select "Регистрация"
4. Enter all required fields
     - First name
     - Last name
     - Email
     - Password
     - Confirm Password
     - Check all mandatory checkboxes with indicated asterisks (*)
5. Select "Регистрация"
- **Expected Result:**
 - User receives a message that they have successfully reistered
 - Website sends out an email to user to confirm identity 
- **Postconditions:** Email is sent out to provided email to confirm identity
- **Status:** ✅ Pass

## Test Case: Login with valid email and password
- **ID:** TC-019
- **Description:** Verify a user can login using valid credentials 
- **Preconditions:** User has an active profile in https://teodor.bg/
- **Test Case Steps:**  
1. Open website
2. Navigate to Login / Registration form
3. Enter email and Password
4. Select "Вход"
- **Expected Result:** User is successfully logged in and redirected to their account dashboard.
- **Status:** ✅ Pass

## Test Case: Login with invalid email
- **ID:** TC-020
- **Description:** Can the user can login using invalid email and valid password 
- **Preconditions:** User has an active profile in https://teodor.bg/
- **Test Case Steps:**  
1. Open website
2. Navigate to Login / Registration form
3. Enter invalid email and valid Password
4. Select "Вход"
- **Expected Result:**
 - User could not log in to their profile
 - An error message is displayed under the email/password fields:"Имейлът или паролата е грешен. Моля, опитайте отново."
- **Status:** ❌ Fail

## Test Case: Login with invalid password
- **ID:** TC-021
- **Description:** Can the user can login using valid email and invalid password 
- **Preconditions:** User has an active profile in https://teodor.bg/
- **Test Case Steps:**  
1. Open website
2. Navigate to Login / Registration form
3. Enter invalid email and valid Password
4. Select "Вход"
- **Expected Result:**
 - User could not log in to their profile
 - An error message is displayed under the email/password fields:"Имейлът или паролата е грешен. Моля, опитайте отново."
- **Status:** ❌ Fail
