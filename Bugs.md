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

The user might abandon the purchase if they don't realize they qualify for free shipping.

🔹 **Suggested Fix**:

Display a banner or pop-up in the cart when the total exceeds 100 BGN.
