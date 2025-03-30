- Bug ID: BUG-0014
- Title: Missing Free Shipping Notification in Cart for Orders Over 100 BGN
- Environment:

**OS**: Windows 11

**Browser**: Chrome Version 132.0.6834.160 (Official Build) (64-bit)

**Website**: https://workout.bg/

🔹 Steps to Reproduce:

1. Open website and navigate to "Вход".
2. Enter valid credentials and log in.
3. Go to "Фитнес добавки".
4. Select "Суроватъчен протеин" that costs more than 100 BGN.
5. Choose a flavor and add the product to the cart.
6. Open the cart and check for free shipping notification.

🔹 **Expected Result**:

✅A notification message should appear in the cart, informing the user that they qualify for free shipping.

✅Example: "Поздравления! Имате право на безплатна доставка за тази поръчка."

🔹 **Actual Result**:

❌No notification appears in the cart.

❌Free shipping is only visible at checkout, which may cause confusion.

🔹 **Severity**: 🟠 Medium (UX/Functionality Issue)

📌The user might abandon the purchase if they don't realize they qualify for free shipping.

🔹 **Suggested Fix**:

Display a banner or pop-up in the cart when the total exceeds 100 BGN.

**-------------------------------------------------------------------------------------------------------------------------------------------------------------**

- Bug ID: BUG-0033
- Title: Increase Quantity to Multiple Items from Favorites
- Environment:

**OS**: Windows 11

**Browser**: Chrome Version 132.0.6834.160 (Official Build) (64-bit)

**Website**: https://teodor.bg/

🔹 **Steps to Reproduce**:

1. Open target URL
2. Navigate to the Login/Registration form.
3. Enter valid credentials and select "Вход".
4. Go to the "Любими" section.
5. Increase the quantity of all items by one.
6. Select "Актуализиране на списък с желани продукти".

🔹 **Expected Result**:

✅ The quantity for each item in "Любими" (Favorites) is successfully increased by one.

✅ A success message appears: "Успешно увеличихте количеството на <артикул> от вашия списък с желани продукти."

🔹 **Actual Result**:

❌ No success message appears.

❌ The system returns an error screen during request processing.

[Video Demonstration of Bug](https://github.com/Drunin-Martin/QA-Test-Cases-and-Bugs/raw/main/Teodor%20%231.mp4)

![Teodor](https://github.com/user-attachments/assets/40ec16f1-ca57-4789-8622-103176e7a5dd)


🔹 **Severity**: 🔴 HIGH (UX/Functionality Issue)

📌 If users encounter an error when updating their wishlist, they might reconsider making a purchase.

🔹 **Suggested Fix**:

✔️ Implement a validation check to define the maximum number of items that can be updated at the same time.

✔️ Ensure that error handling provides a clear user-friendly message instead of a system error screen.

**-------------------------------------------------------------------------------------------------------------------------------------------------------------**

🐞 Bug ID: BUG-0035
-  Title: Select Remove More than Once in Favorites

🖥️**Environment**

**OS**: Windows 11

**Browser**: Chrome Version 132.0.6834.160 (Official Build) (64-bit)

**Website**: https://teodor.bg/

🔹 **Steps to Reproduce**:

1. Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Любими"(Favorites) section
6. Select Trash bin (Remove) two times on given item

✅  **Expected Result**:

- User successfully removed a product in "Любими"(Favorites)

- Trash Bin (Remove) button cannot be selected a second time as it is greyed out

- A success message is displayed :**"Успешно премахнате артикула от вашия списък с желани продукти"**

❌ **Actual Result**:

- We are provided with a 404 Bad Request

📹[Video Demonstration of Bug](https://github.com/Drunin-Martin/QA-Test-Cases-and-Bugs/blob/main/Teodor%20%232.mp4)

![Teodor 404](https://github.com/user-attachments/assets/8de71ae1-4b9e-436b-a079-f4f66fe4172a)

🚨 Severity: 🟠 High (Functionality Issue)

📌 Users may think the website is broken.

📌 Leads to bad user experience and loss of trust.

🛠️ **Suggested Fix:**

✔️ Prevent multiple removals on the same item by disabling the "Remove" button after the first click.

**-------------------------------------------------------------------------------------------------------------------------------------------------------------**

🐞 Bug ID: BUG-0044
- Title: Pagination in Shopping Cart with Manually Increased Item Quantity

🖥️**Environment**

**OS**: Windows 11

**Browser**: Chrome Version 132.0.6834.160 (Official Build) (64-bit)

**Website**: https://teodor.bg/

🔹 **Steps to Reproduce**:

1.Open target URL
2. Navigate to Login / Registration form
3. Enter valid credentials
4. Select "Вход"
5. Go to "Количка" (Shopping Cart) section
6. Increase quantity of any item of choice manually (instead of using + or - buttons)
7. Select page 2 while in "Количка" (Shopping Cart)

✅  **Expected Result**:

 - User successfully increased quantity to item of choice

 - The system saves and reflects the updated quantity

 - Success message is displayed :**"Успешно увеличихте колиеството на <артикул> във вашата количка."**

❌ **Actual Result**:

 - Instead of displaying Page 2, the system shows backend-generated code including JSON and raw HTML

 - The page fails to load properly, making it impossible to view additional cart items

📹[Video Demonstration of Bug](https://github.com/Drunin-Martin/QA-Test-Cases-and-Bugs/blob/main/Teodor%20%233.mp4)

![Teodor JSON](https://github.com/user-attachments/assets/6c56e49e-2787-4f0e-b83a-8f736ef6ffae)


🚨 Severity: 🛑 Blocker (Functionality Issue & Potential Security Risk)

📌 Prevents normal shopping behavior—users cannot navigate cart pages
📌 Potential security issue—exposing internal response structure
📌 Significant UX problem—users may abandon purchases

🛠️ **Suggested Fix:**

✔️ Ensure the backend response correctly renders Shopping Cart pages

✔️ Implement proper validation for manually entered quantities before paginating

✔️ Display a user-friendly error message if input conflicts with pagination
