# Sample Bug Reports

## BUG-001: Cart Count Does Not Update After Removing Item

Severity: High  
Priority: High  
Module: Cart  
Environment: Windows 11, Chrome latest  

Steps to Reproduce:

1. Log in with a valid user.
2. Add two products to the cart.
3. Open the cart page.
4. Remove one product.

Expected Result:

The removed product disappears and the cart badge decreases from 2 to 1.

Actual Result:

The product is removed from the cart page, but the cart badge still shows 2.

Impact:

Users may think the cart still contains removed items, which can reduce checkout confidence.

## BUG-002: Checkout Allows Postal Code With Only Spaces

Severity: Medium  
Priority: Medium  
Module: Checkout  
Environment: Windows 11, Edge latest  

Steps to Reproduce:

1. Add one product to cart.
2. Click Checkout.
3. Enter valid first and last name.
4. Enter three spaces in the postal code field.
5. Click Continue.

Expected Result:

The system should show a validation error for invalid postal code.

Actual Result:

The user is allowed to continue to the order summary.

Impact:

Invalid shipping data may be submitted.

## BUG-003: Product Image Missing on Product Details Page

Severity: Medium  
Priority: Medium  
Module: Product Details  
Environment: Windows 11, Firefox latest  

Steps to Reproduce:

1. Log in.
2. Click any product from the product list.
3. Observe the product details page.

Expected Result:

Product image, name, description, and price are displayed.

Actual Result:

The product image area is blank.

Impact:

Users cannot visually confirm the product before adding it to cart.

## BUG-004: Error Message Is Too Generic For Invalid Login

Severity: Low  
Priority: Medium  
Module: Login  
Environment: Windows 11, Chrome latest  

Steps to Reproduce:

1. Open login page.
2. Enter invalid username and password.
3. Click Login.

Expected Result:

The message clearly explains that the username or password is incorrect.

Actual Result:

The message only says "Error".

Impact:

Poor error feedback may confuse users.

## BUG-005: Checkout Button Overlaps Cart Item Text On Mobile

Severity: High  
Priority: High  
Module: Cart / Mobile UI  
Environment: Chrome mobile viewport, 390 x 844  

Steps to Reproduce:

1. Log in.
2. Add one product with a long name to the cart.
3. Open cart page.
4. Resize browser to mobile width.

Expected Result:

Product information and checkout controls should be readable without overlap.

Actual Result:

The Checkout button overlaps product name text.

Impact:

Mobile users may not be able to read cart contents or proceed comfortably.

Note: Sample bug based on exploratory testing”
