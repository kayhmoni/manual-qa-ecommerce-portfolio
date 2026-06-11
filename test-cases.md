# Manual Test Cases

| ID | Module | Test Scenario | Steps | Expected Result | Priority |
|---|---|---|---|---|---|
| TC-001 | Login | Verify valid user can log in | Open app, enter valid username/password, click Login | User lands on products page | High |
| TC-002 | Login | Verify invalid password is rejected | Enter valid username and invalid password, click Login | Error message is displayed | High |
| TC-003 | Login | Verify empty login form validation | Leave fields blank, click Login | Required-field error is displayed | High |
| TC-004 | Login | Verify logout works | Log in, open menu, click Logout | User returns to login page | Medium |
| TC-005 | Products | Verify product list loads | Log in and view products page | Product names, prices, and images are visible | High |
| TC-006 | Products | Verify product details page opens | Click a product name/image | Product details are displayed | Medium |
| TC-007 | Products | Verify sorting by price low to high | Select price low-to-high sorting | Products are sorted correctly | Medium |
| TC-008 | Products | Verify sorting by name A-Z | Select name A-Z sorting | Products are sorted alphabetically | Medium |
| TC-009 | Cart | Verify item can be added to cart | Click Add to Cart for one product | Cart badge updates and button state changes | High |
| TC-010 | Cart | Verify multiple items can be added | Add two or more products | Cart badge shows correct item count | High |
| TC-011 | Cart | Verify item can be removed from product page | Add item, click Remove | Item is removed and cart count updates | Medium |
| TC-012 | Cart | Verify cart page displays added items | Add item, open cart | Correct item name, quantity, and price are shown | High |
| TC-013 | Cart | Verify item can be removed from cart page | Open cart, click Remove | Item no longer appears in cart | High |
| TC-014 | Checkout | Verify checkout starts with cart item | Add item, open cart, click Checkout | Checkout information page opens | High |
| TC-015 | Checkout | Verify first name is required | Leave first name blank, complete other fields, continue | First-name error is displayed | High |
| TC-016 | Checkout | Verify last name is required | Leave last name blank, complete other fields, continue | Last-name error is displayed | High |
| TC-017 | Checkout | Verify postal code is required | Leave postal code blank, complete other fields, continue | Postal-code error is displayed | High |
| TC-018 | Checkout | Verify valid checkout information continues | Enter valid first name, last name, postal code | Order summary page opens | High |
| TC-019 | Checkout | Verify order summary prices | Reach summary page | Item total, tax, and total are displayed correctly | High |
| TC-020 | Checkout | Verify order can be completed | Click Finish on summary page | Confirmation message is displayed | High |
| TC-021 | Checkout | Verify cancel from checkout returns correctly | Start checkout, click Cancel | User returns to cart or products page as designed | Medium |
| TC-022 | UI | Verify responsive layout on mobile width | Resize browser to mobile viewport | Content remains readable and usable | Medium |
| TC-023 | UI | Verify buttons have clear states | Add/remove products and observe buttons | Button text and state are clear | Low |
| TC-024 | Regression | Verify full purchase flow after changes | Login, add item, checkout, finish order | End-to-end flow completes successfully | High |
| TC-025 | Accessibility | Verify keyboard navigation basic flow | Use Tab and Enter through main flow | User can reach key controls without mouse | Medium |

