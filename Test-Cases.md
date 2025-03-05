## Login // Logout // Registration
- **Target website:** https://workout.bg/
## Test Case: Login with valid credentials
- **ID:** TC-001
- **Description:** Login with valid credentials
- **Preconditions:** User has an active profile in https://workout.bg/
- **Test Case Steps:**
  1. Open website and navigate to "Вход"
  2. Enter valid email & password
  3. Select "Влез"
- **Expected Result:** User successfully logged in
- **Status:** ✅ Pass

## Test Case: Login with invalid email
- **ID:** TC-002
- **Description:** Login with invalid email 
- **Preconditions:** User has an active profile in https://workout.bg/
- **Test Case Steps:**  
  1. Open website and navigate to "Вход"
  2. Enter invalid email & valid password
  3. Select "Влез"
- **Expected Result:** The system should display an error message: "Грешен имейл или парола."
- **Status:** ❌ Fail

## Test Case: Login with invalid password
- **ID:** TC-003
- **Description:** Login with invalid password 
- **Preconditions:** User has an active profile in https://workout.bg/
- **Test Case Steps:**  
  1. Open website and navigate to "Вход"
  2. Enter valid email & invalid password
  3. Select "Влез"
- **Expected Result:** The system should display an error message: "Грешен имейл или парола."
- **Status:** ❌ Fail

## Test Case: Login with Google Account  
- **ID:** TC-004
- **Description:** Login with Google Account
- **Preconditions:** User has a Google Account
- **Test Case Steps:**
  1. Open website https://workout.bg/ and navigate to "Вход"
  2. Navigate to "Вход с Google"
- **Expected Result:** User successfully logged in with Google Account
- **Status:** ✅ Pass

## Test Case: Add Valid Telephone in Profile  
- **ID:** TC-005
- **Description:** Add valid telephone in profile
- **Preconditions:** User has an active profile in https://workout.bg/
- **Test Case Steps:**
  1. Open website https://workout.bg/ and navigate to "Вход"
  2. Enter valid credentials
  3. Select "Влез"
  4. Navigate to "Профил"
  5. Select "Редакция"
  6. Enter valid "Телефон" number
  7. Enter "Продължете"
- **Expected Result:** User added telephone number
- **Status:** ✅ Pass

## Test Case: Add Invalid Telephone in Profile  
- **ID:** TC-006
- **Description:** Add an Invalid telephone in profile
- **Preconditions:** User has an active profile in https://workout.bg/
- **Test Case Steps:**
  1. Open website and navigate to "Вход"
  2. Enter valid credentials
  3. Select "Влез"
  4. Navigate to "Профил"
  5. Select "Редакция"
  6. Enter invalid "Телефон" number
  7. Enter "Продължете"
- **Expected Result:** User provided with warning message: "Телефонният номер трябва да съдържа между 10 и 32 символа."
- **Status:** ❌ Fail

## Test Case: Add Text in Telephone Field  
- **ID:** TC-007
- **Description:** Add Text in Telephone Field
- **Preconditions:** User has an active profile in https://workout.bg/
- **Test Case Steps:**
  1. Open website and navigate to "Вход"
  2. Enter valid credentials
  3. Select "Влез"
  4. Navigate to "Профил"
  5. Select "Редакция"
  6. Enter text in "Телефон" field
  7. Enter "Продължете"
- **Expected Result:** User should be able to input only numerals in telephone field
- **Status:** ❌ Fail

## Test Case: Registration with valid details
- **ID:** TC-008
- **Description:** Registration with valid details
- **Preconditions:** User does not have an account
- **Test Case Steps:**
  1. Open website https://workout.bg/ and navigate to "Регистрация"
  2. Enter all mandatory fields
     - Име: "Георги"  
     - Фамилия: "Петров" 
     - Телефон: "0895 111 222"  
     - Email: "georgi.petrov@gmail.com" 
     - Парола: "Georgi123@"
  3. Check the box "Прочетох и съм съгласен със Защита на личните данни (GDPR)"
  4. Select "Продължете"
- **Expected Result:** User successfully registered
- **Status:** ✅ Pass
- **Postconditions:** The user is redirected to the Homepage. 

## Test Case: Registration with invalid details  
- **ID:** TC-009  
- **Description:** Attempt to register with invalid details  
- **Preconditions:** User does not have an existing account  
- **Test Case Steps:**  
  1. Open website https://workout.bg/ and navigate to "Регистрация"  
  2. Enter the following invalid details in the mandatory fields:  
     - Име: "A" (too short)  
     - Фамилия: "B" (too short)  
     - Телефон: "123" (less than 10 digits)  
     - Email: "invalidemail.com" (missing @)  
     - Парола: "123" (too short)  
  3. Check the box "Прочетох и съм съгласен със Защита на личните данни (GDPR)"  
  4. Select "Продължете"  
- **Expected Result:**  
  - The system should display an error message under each invalid field:  
    - "Името трябва да бъде между 5 и 20 символа"  
    - "Фамилията трябва да бъде между 5 и 20 символа"  
    - "Телефонът трябва да съдържа между 10 и 32 символа"  
    - "Невалиден e-mail адрес!"  
    - "Паролата трябва да бъде между 5 и 20 символа"  
- **Status:** ❌ Fail  
- **Postconditions:** The user remains on the registration page and the form is not submitted.

## Test Case: Reset Password via Email
- **ID:** TC-010
- **Description:** User has forgotten their password
- **Preconditions:** User has an existing account
- **Test Case Steps:**
  1. Open website https://workout.bg/ and navigate to "Вход"
  2. Select "Забравена парола"
  3. Enter registered email address (e.g. `georgi.petrov@gmail.com`)
  4. Select "Продължете"
  5. Open the inbox and locate the password reset email  
  6. Click the link inside the email  
  7. Enter a new password and confirm  
  8. Click "Запази"
- **Expected Result:**
  - System displays a confirmation message: **"Имейлът за възстановяване на парола беше изпратен"**  
  - User receives an email with subject: **"Възстановяване на паролата – Workout.bg"**  
  - After setting a new password, the system confirms: **"Паролата е променена успешно"**
- **Status:** ✅ Pass
- **Postconditions:**
  - User can login with new password  
  - Old password is no longer valid

## Shopping Cart

## Test Case: Add Item(s) to Cart
- **ID:** TC-011
- **Description:** Add Item(s) to Cart
- **Preconditions:** User has an active profile in https://workout.bg/
- **Test Case Steps:**
1. Open website https://workout.bg/ and navigate to "Вход"
2. Enter valid details
3. Select "Влез"
4. Go to "Фитнес добавки"
5. Navigate to "Суроватъчен протеин" and select first item
6. Input "Вкус" and valid quantity
7. Enter "Кошница"
- **Expected Result:** User should see the desired item with the desired "Вкус" and quantity being added successfully in "Kошница"
- **Status:** ✅ Pass


## Test Case: Remove Item(s) from Cart
- **ID:** TC-012
- **Description:** Remove Item(s) from Cart
- **Preconditions:** User has an active profile in https://workout.bg/
- **Test Case Steps:**
1. Open website https://workout.bg/ and navigate to "Вход"
2. Enter valid details
3. Select "Влез"
4. Go to "Фитнес добавки"
5. Navigate to "Суроватъчен протеин" and select first item
6. Input "Вкус" and valid quantity
7. Enter "Кошница"
8. Remove item from "Кошница"
9. Navigate to homepage
- **Expected Result:** User should see "Kошница" as empty from homepage
- **Status:** ✅ Pass


## Test Case: Warning Message for Exceeding Available Quantity
- **ID:** TC-013
- **Description:** Verify that the system displays a warning message when a user tries to add more items to the cart than are available in stock.
- **Preconditions:** 
- User has an active profile in https://workout.bg/
- The selected product has a stock limit (e.g., max available = 5 units)
- **Test Case Steps:**
1. Open website https://workout.bg/ and navigate to "Вход"
2. Enter valid credentials
3. Select "Влез"
4. Go to "Фитнес добавки"
5. Navigate to "Суроватъчен протеин" and select first item
6. Choose a flavor from the "Вкус" dropdown (e.g., "Ванилия")
7. In the quantity field, enter **a number greater than the available stock** (e.g., 99 if the stock is 5)
8. Add item to cart from "Купи" button
- **Expected Result:** User receives a warning message from the website that the desired quantity is not available
- **Status:** ❌ Fail

## Test Case: Automatic Free Shipping Notification for Orders Over 100 BGN
- **ID:** TC-014
- **Description:** Ensure that when a user adds items worth more than 100 BGN to the cart, the system automatically displays a notification informing them that they qualify for free shipping.
- **Preconditions:** 
- User has an active profile in https://workout.bg/
- User has added products **worth more** than 100 BGN to the cart.
- **Test Case Steps:**
1. Open website https://workout.bg/ and navigate to "Вход"
2. Enter valid credentials
3. Select "Влез"
4. Go to "Фитнес добавки"
5. Navigate to "Суроватъчен протеин" and select first item that costs more than 100 BGN
6. Choose a flavor from the "Вкус" dropdown (e.g., "Ванилия")
7. Add item to cart from "Купи" button
- **Expected Result:** User receives a notification message from the website that they can now take advantage of free shipping of given product(s)
- **Status:** ❌ Fail
