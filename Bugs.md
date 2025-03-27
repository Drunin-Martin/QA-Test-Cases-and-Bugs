- Bug ID: BUG-0014
- Title: Missing Free Shipping Notification in Cart for Orders Over 100 BGN
- Environment:

**OS**: Windows 11

**Browser**: Chrome Version 132.0.6834.160 (Official Build) (64-bit)

**Website**: https://workout.bg/

🔹 Steps to Reproduce:

Open website and navigate to "Вход".
Enter valid credentials and log in.
Go to "Фитнес добавки".
Select "Суроватъчен протеин" that costs more than 100 BGN.
Choose a flavor and add the product to the cart.
Open the cart and check for free shipping notification.

🔹 **Expected Result**:

A notification message should appear in the cart, informing the user that they qualify for free shipping.
Example: "Поздравления! Имате право на безплатна доставка за тази поръчка."

🔹 **Actual Result**:

No notification appears in the cart.
Free shipping is only visible at checkout, which may cause confusion.

🔹 **Severity**: 🟠 Medium (UX/Functionality Issue)

- Bug ID: BUG-0033
- Title: Increase Quantity to Multiple Items from Favorites
- Environment:

**OS**: Windows 11

**Browser**: Chrome Version 132.0.6834.160 (Official Build) (64-bit)

**Website**: https://teodor.bg/

🔹 Steps to Reproduce:

Open website and navigate to Login / Registration form.
Enter valid credentials and log in.
Select "Вход".
Go to "Любими"(Favorites) section
Increase quantity to all items by one
Select "Актуализиране на списък с желани продукти"

🔹 **Expected Result**:

User successfully increased the quantity by one for each item from "Любими"(Favorites)
Success message is displayed :**"Успешно увеличихте количестовото на <артикул> от вашия списък с желани продукти."**

🔹 **Actual Result**:

No notification appears in "Любими"(Favorites).
We are provided with an error screen when our request was being processed.
![Teodor](https://github.com/user-attachments/assets/40ec16f1-ca57-4789-8622-103176e7a5dd)


🔹 **Severity**: 🟠 Medium (UX/Functionality Issue)

The user might abandon the purchase if they don't realize they qualify for free shipping.

🔹 **Suggested Fix**:

Display a banner or pop-up in the cart when the total exceeds 100 BGN.


The user might abandon the purchase if they don't realize they qualify for free shipping.

🔹 **Suggested Fix**:

Display a banner or pop-up in the cart when the total exceeds 100 BGN.
