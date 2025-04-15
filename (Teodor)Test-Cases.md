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
1. Open target URL
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
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid email
4. Leave password field blank
5. Select "Вход"
- **Expected Result:**
 - User cannot log in to their profile
 - An error message is displayed under the password field:**"Моля въведете парола."**
- **Status:** ✅ Pass

## Favorites

## Test Case: Add an Item to Favorites
- **ID:** TC-028
- **Description:** Add any item on the product page and add it to Favorites
- **Preconditions:** User has an active profile in https://teodor.bg/
- **Test Case Steps:**
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Аксесоари"
6. Find "Папийонки"
7. Open any product of random choice
8. Add the item of choice to "Добави в любими"
- **Expected Result:**
 - User successfully added product of choice in "Любими"(Favorites)
 - Website automatically redirects user to "Любими"(Favorites) when an Item is added
 - A success message is displayed :**"Успешно добавихте артикула във вашия списък с желани продукти"**
- **Status:** ✅ Pass

## Test Case: Remove an Item from Favorites
- **ID:** TC-029
- **Description:** Remove an item from "Любими"(Favorites)
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has at least one item added to "Любими"(Favorites)
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Любими"(Favorites) section
6. Select Trash bin (Remove) on the item 
- **Expected Result:**
 - User successfully removed a product in "Любими"(Favorites)
 - A success message is displayed :**"Успешно премахнате артикула от вашия списък с желани продукти"**
- **Status:** ✅ Pass

## Test Case: Add One Item from Favorites to Shopping Cart
- **ID:** TC-030
- **Description:** Add an item from Favorites to Shopping Cart 
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has at least one item added to "Любими"(Favorites)
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Любими"(Favorites) section
6. Select "Добави"(Add) to Shopping Cart 
- **Expected Result:**
 - User successfully added a product from "Любими"(Favorites) to Shopping Cart
 - Success message is displayed :**"Успешно добавихте артикула от вашия списък с желани продукти в количката."**
- **Status:** ✅ Pass

## Test Case: Add Multiple Items from Favorites to Shopping Cart
- **ID:** TC-031
- **Description:** Add multiple items from Favorites to Shopping Cart 
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has a few items added to "Любими"(Favorites)
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Любими"(Favorites) section
6. Select "Добави всички в количката"
7. Navigate to "Количка"(Shopping Cart)
- **Expected Result:**
 - User successfully added all products from "Любими"(Favorites) to Shopping Cart
 - The number of items added from "Любими"(Favorites) to "Количка"(Shopping Cart) is the same
 - Success message is displayed :**"Успешно добавихте артикулите от вашия списък с желани продукти в количката."**
- **Status:** ✅ Pass

## Test Case: Increase Quantity to One Item from Favorites
- **ID:** TC-032
- **Description:** Increase quantity to one of the items from Favorites 
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has a few items added to "Любими"(Favorites)
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Любими"(Favorites) section
6. Increase quantity to one item of choice
7. Select "Актуализиране на списък с желани продукти"
- **Expected Result:**
 - User successfully increased the size to one item of choice from "Любими"(Favorites)
 - Success message is displayed :**"Успешно увеличихте количестовото на <артикул> от вашия списък с желани продукти."**
- **Status:** ✅ Pass

## Test Case: Increase Quantity to Multiple Items from Favorites
- **ID:** TC-033
- **Description:** Increase quantity to multiple Items from Favorites 
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has a few items added to "Любими"(Favorites)
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Любими"(Favorites) section
6. Increase quantity to all items by one
7. Select "Актуализиране на списък с желани продукти"
- **Expected Result:**
 - User successfully increased the size to one item of choice from "Любими"(Favorites)
 - Success message is displayed :**"Успешно увеличихте количестовото на <артикул> от вашия списък с желани продукти."**
- **Status:** ❌ Fail
- **Linked Bug** [BUG-0033] (https://github.com/Drunin-Martin/QA-Test-Cases-and-Bugs/blob/main/Bugs.md)

## Test Case: Increase Quantity to All Items from Favorites and Add to Shopping Cart
- **ID:** TC-034
- **Description:** Increase Quantity to All Items from Favorites and Add to Shopping Cart 
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has a few items added to "Любими"(Favorites)
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Любими"(Favorites) section
6. Increase quantity to all items by one
7. Select "Актуализиране на списък с желани продукти"
8. Select "Добави всички към количката"
- **Expected Result:**
 - User successfully increased the quantity for all items in "Любими" (Favorites)
 - Success message is displayed :**"Успешно увеличихте количестовото на <артикул> от вашия списък с желани продукти."**
 - User successfully adds all items to the shopping cart
- **Actual Result:**
- The system does not update the quantity for the items.
- No success message appears.
- An error screen appears when trying to process the request.
**Failure Reason:** This test case fails due to [BUG-0033]
- **Status:** ❌ Fail
- **Linked Bug** [BUG-0033] (https://github.com/Drunin-Martin/QA-Test-Cases-and-Bugs/blob/main/Bugs.md)

## Test Case: Select Remove More than Once in Favorites
- **ID:** TC-035
- **Description:** Remove an item from "Любими"(Favorites) 
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has at least one item added to "Любими"(Favorites)
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Любими"(Favorites) section
6. Select Trash bin (Remove) two times on given item 
- **Expected Result:**
 - User successfully removed a product in "Любими"(Favorites)
 - Trash Bin (Remove) button cannot be selected a second time as it is greyed out
 - A success message is displayed :**"Успешно премахнате артикула от вашия списък с желани продукти"**
- **Status:** ❌ Fail
- **Linked Bug** [BUG-0035] (https://github.com/Drunin-Martin/QA-Test-Cases-and-Bugs/blob/main/Bugs.md)

## Shopping Cart

## Test Case: Add Item to Shopping Cart
- **ID:** TC-036
- **Description:** Add Item to Shopping Cart
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Аксесоари" section
6. Navigate to "Папийонки"
7. Open Item of choice
8. Select "Добави"
- **Expected Result:**
 - User successfully added an item of choice to "Количка" (Shopping Cart)
 - Success message is displayed :**"Успешно добавихте <артикул> във вашата количка."**
- **Status:** ✅ Pass

## Test Case: Remove Item from Shopping Cart
- **ID:** TC-037
- **Description:** Remove Item from Shopping Cart
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Аксесоари" section
6. Navigate to "Папийонки"
7. Open Item of choice
8. Select "Добави"
9. Enter "Количка"(Shopping Cart)
- **Expected Result:**
 - User successfully added an item of choice to "Количка" (Shopping Cart)
 - Success message is displayed :**"Успешно добавихте <артикул> във вашата количка."**
 - Once the user navigates to "Количка" (Shopping Cart) the desired item of choice is present
- **Status:** ✅ Pass

## Test Case: Add Item to Shopping Cart w/ No Profile
- **ID:** TC-038
- **Description:** Add Item to Shopping Cart
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Аксесоари" section
6. Navigate to "Папийонки"
7. Open Item of choice
8. Select "Добави"
- **Expected Result:**
 - User successfully added an item of choice to "Количка" (Shopping Cart)
 - Success message is displayed :**"Успешно добавихте <артикул> във вашата количка."**
- **Status:** ✅ Pass

## Test Case: Remove Item from Shopping Cart w/ No Profile
- **ID:** TC-039
- **Description:** Remove Item from Shopping Cart
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Аксесоари" section
6. Navigate to "Папийонки"
7. Open Item of choice
8. Select "Добави"
9. Enter "Количка"(Shopping Cart)
- **Expected Result:**
 - User successfully added an item of choice to "Количка" (Shopping Cart)
 - Success message is displayed :**"Успешно добавихте <артикул> във вашата количка."**
 - Once the user navigates to "Количка" (Shopping Cart) the desired item of choice is present
- **Status:** ✅ Pass

## Test Case: Increase Quantity from Within Shopping Cart
- **ID:** TC-040
- **Description:** Increase Quantity from Within Shopping Cart
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has at least one item added to "Количка" (Shopping Cart)
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Количка" (Shopping Cart)" section
6. Increase quantity of said item
- **Expected Result:**
 - User successfully added an item of choice to "Количка" (Shopping Cart)
 - Success message is displayed :**"Успешно увеличихте количеството на <артикул> във вашата количка."**
- **Status:** ✅ Pass

## Test Case: Decrease Quantity from Within Shopping Cart
- **ID:** TC-041
- **Description:** Decrease Quantity from Within Shopping Cart
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has at least one item added to "Количка" (Shopping Cart)
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Количка" (Shopping Cart)" section
6. Increase quantity of said item by +1
7. Decrease quantity of said item by -1
- **Expected Result:**
 - User successfully increased quantity of an item of choice in "Количка" (Shopping Cart)
 - User successfully decreased quantity of an item of choice in "Количка" (Shopping Cart)
 - Success message is displayed :**"Успешно увеличихте количеството на <артикул> във вашата количка."**
 - Success message is displayed :**"Успешно намалихте количеството на <артикул> във вашата количка."**
- **Status:** ✅ Pass

## Test Case: Increase Quantity Manually from Within Shopping Cart
- **ID:** TC-042
- **Description:** Increase Quantity Manually from Within Shopping Cart
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has at least one item added to "Количка" (Shopping Cart)
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Количка" (Shopping Cart)" section
6. Increase quantity of said item by writing it out in Quantity field
- **Expected Result:**
 - User successfully added an item of choice to "Количка" (Shopping Cart)
 - Success message is displayed :**"Успешно увеличихте количеството на <артикул> във вашата количка."**
- **Status:** ✅ Pass

## Test Case: Decrease Quantity Manually from Within Shopping Cart
- **ID:** TC-043
- **Description:** Decrease Quantity Manually from Within Shopping Cart
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has at least one item added to "Количка" (Shopping Cart)
- **Test Case Steps:**  
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Количка" (Shopping Cart)" section
6. Increase quantity of said item by writing it out in Quantity field
7. Decrease quantity of said item by writing it out in Quantity field
- **Expected Result:**
 - User successfully increased quantity of an item of choice in "Количка" (Shopping Cart)
 - User successfully decreased quantity of an item of choice in "Количка" (Shopping Cart)
 - Success message is displayed :**"Успешно увеличихте количеството на <артикул> във вашата количка."**
 - Success message is displayed :**"Успешно намалихте количеството на <артикул> във вашата количка."**
- **Status:** ✅ Pass


## Test Case: Pagination in Shopping Cart with Manually Increased Item Quantity
- **ID:** TC-044
- **Description:** Trigger pagination in Shopping Cart
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- User has 42+ items added in "Количка" (Shopping Cart)
- **Test Case Steps:**
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Количка" (Shopping Cart) section
6. Increase quantity of any item of choice manually (instead of using + or - buttons)
7. Select page 2 while in "Количка" (Shopping Cart)
- **Expected Result:**
 - User successfully increased quantity to item of choice
 - The system saves and reflects the updated quantity
 - Success message is displayed :**"Успешно увеличихте колиеството на <артикул> във вашата количка."**
- **Status:** ❌ Fail
- **Linked Bug** [BUG-0044] (https://github.com/Drunin-Martin/QA-Test-Cases-and-Bugs/blob/main/Bugs.md)

## Test Case: Shopping Cart Behavior for Multiple Items of Same Type but Different Sizes
- **ID:** TC-045
- **Description:** Multiple items of the same type in Shopping Cart but different in size
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- **Test Case Steps:**
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Облекло" and select "Сака"
6. Open any Item of choice 
7. Select any size and enter "Добави"
8. While on same Item, enter a different size and enter "Добави"
9. Navigate to "Количка" (Shopping Cart)
- **Expected Result:**
 - Both items appear as separate entries in the Shopping Cart
 - Success message is displayed :**"Успешно добавихте <артикул> във вашата количка."**
- **Status:** ✅ Pass

## Test Case: Item Behavior When Chosen Quantity Exceeds Available Stock
- **ID:** TC-046
- **Description:** Chosen quantity exceeding available stock 
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- **Test Case Steps:**
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Облекло" and select "Сака"
6. Open any Item of choice 
7. Select any size and enter "Добави"
8. Navigate to "Количка" (Shopping Cart)
9. Increase the quantity of the item above the available stock
- **Expected Result:**
 - A success message is displayed :**"Успешно увеличихте колиеството на <артикул> във вашата количка."**
 - A stock availability threshold message is displayed: **"Исканото количество не е налично."**
 - User cannot increase the quantity beyond the available stock (button is disabled or input is corrected).
- **Status:** ❌ Fail

## Test Case: Apply Valid Promo Code in Shopping Cart Section
- **ID:** TC-047
- **Description:** Input valid promo code
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- **Test Case Steps:**
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials and select "Вход"
4. Hover over "Облекло" and select "Ризи"
5. Open any item of choice, enter size and input "Добави"
6. Go to "Количка" (Shopping Cart)
7. Locate the promo code input field
8. Enter Promo Code "TEODOR10" and choose "Приложи"
- **Expected Result:**
 - A success message is displayed :**"Успешно приложихте Вашият промо код."**
 - The Item price is reduced by 10% off on chosen Item
- **Status:** ✅ Pass

## Test Case: Apply Invalid Promo Code in Shopping Cart Section
- **ID:** TC-048
- **Description:** Input invalid promo code
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- **Test Case Steps:**
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials and select "Вход"
4. Go to "Облекло" and select "Ризи"
5. Open any item of choice, enter size and input "Добави"
6. Navigate to "Количка" (Shopping Cart)
7. Locate the promo code input field
8. Enter the following Promo Code and choose "Приложи":

  - **Non-existent Code**: Enter "XYZ123" and "Приложи"(Apply)

  - **Partially Correct Code**: Enter "TEODOR" and "Приложи"(Apply)

  - **Expired Code**: Enter "TEODOR2024" and "Приложи"(Apply)

  - **Already Used Code**: Enter "TEODOR10" (again) and "Приложи"(Apply)

  - **Empty Field**: Leave blank and "Приложи"(Apply)

  - **Lowercase Code**: Enter "teodor10" and "Приложи"(Apply)

  - **Code with Special Characters**: Enter "TEODOR10!"and "Приложи"(Apply)

  - **Code with Spaces**: Enter " TEODOR10 " and "Приложи"(Apply)

  - **Long Code**: Enter "TEODOR123123123123123123" and "Приложи"(Apply)

- **Expected Result:**
 - System should reject each Invalid Promo Code with relevant error message
 - Input field should prevent special characters from being entered
 - Price remains the same
 - No discount is applied
- **Status:** ✅ Pass

## Test Case: Receive Free Shipping for Orders Over 150BGN
- **ID:** TC-049
- **Description:** Receive free shipping for orders over 150BGN
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- **Test Case Steps:**
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Облекло" and select "Сака"
6. Open an Item with Price over 150BGN 
7. Select any size and enter "Добави"
8. Navigate to "Количка" (Shopping Cart)
- **Expected Result:**
 - For orders above 150 BGN, free shipping should be applied to the cart during checkout.
 - For orders below 150 BGN, no free shipping should be applied.
 - User should receive free shipping due to Item is over 150 BGN
- **Status:** ✅ Pass

## Test Case: Receive Free Shipping for Orders Under 150BGN
- **ID:** TC-050
- **Description:** Receive free shipping for orders under 150BGN
- **Preconditions:**
- User has an active profile in https://teodor.bg/
- **Test Case Steps:**
1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to Search field and enter "149"
6. Select "Виж всички <брой резултати> резултата"
7. Open any Item with a Price of 149BGN 
8. Select any size and enter "Добави"
9. Navigate to "Количка" (Shopping Cart)
- **Expected Result:**
 - User should receive free shipping despite Item being under 150 BGN mark
- **Status:** ✅ Pass

## Search Field

## Test Case: Search Displays Results for Valid Keyword Input
- **ID:** TC-051
- **Description:** Does the search function return relevant results matching the entered keyword

- **Test Case Steps:**
1. Open target URL - https://teodor.bg/
2. Navigate Search field
3. Enter keyword "шапка"
4. Select "Виж всички <брой резултати> резултата"

- **Expected Result:**
 - Search function provides all results under specified keyword
 - Search results number matches actual results displayed in "Виж всички <брой резултати> резултата"
- **Status:** ✅ Pass

## Test Case: Search Displays No Results Message for Invalid Keyword
- **ID:** TC-052
- **Description:** Will the system display an appropriate message when searching for a non-existent product.

- **Test Case Steps:**
1. Open target URL - https://teodor.bg/
2. Navigate Search field
3. Enter keyword "часовник"

- **Expected Result:**
 - The search function does not display any search results.
 - A message is shown, informing the user that there are no matches.
- **Status:** ✅ Pass

## Test Case: Search by Material Provides Correct Results
- **ID:** TC-053
- **Description:** Can the search function provide results for a specific material

- **Test Case Steps:**
1. Open target URL - https://teodor.bg/
2. Navigate Search field
3. Enter keyword "памук"

- **Expected Result:**
 - The search function provides results corresponding to keyword.
 - Number of search results matches actual results displayed in "Виж всички <брой резултати> резултата"
- **Status:** ✅ Pass

## Test Case: Search by Number Provides Correct Results
- **ID:** TC-054
- **Description:** Can the search function provide results using a number

- **Test Case Steps:**
1. Open target URL - https://teodor.bg/
2. Navigate Search field
3. Enter keyword "100"

- **Expected Result:**
  - The search function provides results corresponing to keyword.
  - Number of search results matches actual results displayed in "Виж всички <брой резултати> резултата"
- **Status:** ✅ Pass

## Test Case: Search Field Loses Focus and Becomes Unresponsive
- **ID:** TC-055
- **Description:** Will the search field maintain focus and allow continuous input after highlighting text.

- **Test Case Steps:**
1. Open target URL - https://teodor.bg/
2. Navigate Search field
3. Enter keyword of choice
4. Highlight keyword with intent to copy text
5. Select outside the search field and attempt to continue typing without reselecting it.

- **Expected Result:**
 - The search field should retain focus, allowing the user to continue typing without interruption.
- **Status:** ❌ Fail
- **Linked Bug** [BUG-0055] (https://github.com/Drunin-Martin/QA-Test-Cases-and-Bugs/blob/main/Bugs.md)
