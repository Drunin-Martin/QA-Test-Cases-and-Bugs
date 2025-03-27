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

## Test Case: Register with an Email Already in Use
- **ID:** TC-022
- **Description:** Can the user can register using an email that is already in use 
- **Preconditions:** User does not have a profile in https://teodor.bg/
- **Test Case Steps:**  
1. Open website
2. Navigate to Login / Registration form
3. Select "Регистрация"
4. Enter all required fields
     - First name
     - Last name
     - Email that is already in use
     - Password
     - Confirm Password
     - Check all mandatory checkboxes with indicated asterisks (*)
5. Create new profile from "Регистрация"
- **Expected Result:**
 - User is not able to register new profile due to provided email is already in use
 - An error message is displayed under the email fields:"Този имейл вече се използва. Моля въведете друг имейл."
- **Status:** ❌ Fail

## Test Case: Reset Password from the "Forgotten Password" Feature
- **ID:** TC-023
- **Description:** Can the user update their password using the "Forgotten Password" option
- **Preconditions:** User has an active profile in https://teodor.bg/
- **Test Case Steps:**
1. Open target URL
2. Navigate to the Login/Registration form
3. Click on "Забравена парола"
4. Enter the email associated with the profile
5. Click "Изпрати" (Submit)
6. Open the received email from Teodor
7. Click the reset password link in the email
8. Enter and confirm a new password
9. Click "Запази" (Save)
10. Return to the Login page
11. Enter email and new password
12. Click "Вход" (Login)
- **Expected Result:**
 - The system successfully updates the user’s password
 - The user can log in with the new password without issues
- **Status:** ✅ Pass

## Test Case: Send Reset Password from "Forgotten Password" to invalid Email
- **ID:** TC-024
- **Description:** Can the user enter invalid email for password reset from the "Forgotten Password"
- **Preconditions:** User has an active profile in https://teodor.bg/
- **Test Case Steps:**
1. Open target URL
2. Navigate to the Login/Registration form
3. Click on "Забравена парола"
4. Enter invalid email (Example: `invalidemail@`, `user@invalid`, `test@teodor.bgg`)
5. Click "Изпрати" (Submit)
- **Expected Result:**
 - The system displays an error message:**"Въведеният имейл не съществува. Моля, опитайте отново с валиден имейл."**
 - The password reset process does not continue.
 - The system prompts the user to enter a valid email for password reset
- **Status:** ❌ Fail

## Test Case: Change Current Email with a New Email
- **ID:** TC-025
- **Description:** Change email address for an existing profile 
- **Preconditions:**
  - User has an active profile in https://teodor.bg/
  - User has access to their current email.
  - The new email is not already associated with another account.

- **Test Case Steps:**
1. Open target URL
2. Navigate to the Login/Registration form.
3. Enter valid credentials (current email and password).
4. Click "Вход"
5. Navigate to "Настройки на профил"
6. Click on "Промени Email" (Change Email)
7. Enter a **new valid email address** (different from the current one)
8. Enter the **current password** for verification
9. Click "Запази"
10. System sends a **confirmation email** to the new address (if applicable)
11. Open the confirmation email and click the verification link (if required)
- **Expected Result:**
 - The system displays a message:**"Вашият имейл е обновен успешно."**
 - If email confirmation is required, the system sends a **verification link** to the new email.
 - Logging in with the old email should no longer be possible.
 - Logging in with the new email should be successful.
- **Status:** ✅ Pass

## Test Case: Empty Email Login
- **ID:** TC-026
- **Description:** Login by only entering a password and no email 
- **Preconditions:** User has an active profile in https://teodor.bg/
- **Test Case Steps:**  
1. Open website
2. Navigate to Login / Registration form
3. Leave email field blank
4. Enter valid password 
5. Select "Вход"
- **Expected Result:**
 - User cannot log in to their profile
 - An error message is displayed under the email field:**"Моля въведете имейл."**
- **Status:** ✅ Pass

## Test Case: Empty Password Login
- **ID:** TC-027
- **Description:** Login by only entering an email and no password 
- **Preconditions:** User has an active profile in https://teodor.bg/
- **Test Case Steps:**  
1. Open website
2. Navigate to Login / Registration form
3. Enter valid email
4. Leave password field blank
5. Select "Вход"
- **Expected Result:**
 - User cannot log in to their profile
 - An error message is displayed under the password field:**"Моля въведете парола."**
- **Status:** ✅ Pass
