# 🧪 Test Cases – SauceDemo

This document contains detailed functional test cases designed to validate key user flows of the [SauceDemo](https://www.saucedemo.com/) demo e-commerce application.

> This is a personal learning project based on manual testing practices.

---

## 🔍 Functional Test Suite

| ID     | Title                                                      | Preconditions                  | Steps                                                                                       | Expected Result                                                 | Actual Result  | Status | Priority | Severity |
|--------|------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------|--------|----------|----------|
| TC001  | Login with valid standard credentials                      | `standard_user` account exists | 1. Navigate to login page  2. Enter valid credentials  3. Click "Login"                     | User is redirected to inventory page                            | -              | -      | High     | Major    |
| TC002  | Login with locked-out user                                 | `locked_out_user` exists       | 1. Navigate to login page  2. Enter locked out user credentials  3. Click "Login"           | Error message: "Sorry, this user has been locked out."          | -              | -      | High     | Major    |
| TC003  | Login with empty fields                                    | N/A                            | 1. Navigate to login page  2. Leave both fields empty  3. Click "Login"                     | Error message: "Username is required"                           | -              | -      | High     | Major    |
| TC004  | Add single item to cart from inventory page                | Logged in as standard_user     | 1. Login  2. Click "Add to cart" on item X                                                  | Button label changes to "Remove", cart count updates to 1       | -              | -      | Medium   | Minor    |
| TC005  | Remove item from cart on cart page                         | Item added to cart             | 1. Go to cart  2. Click "Remove" next to item                                               | Item is removed, cart count updates                             | -              | -      | Medium   | Minor    |
| TC006  | Sort products by Price (low to high)                       | Logged in                      | 1. Login  2. Open sort dropdown  3. Select "Price (low to high)"                            | Product list is reordered from lowest to highest price          | -              | -      | Medium   | Minor    |
| TC007  | Attempt checkout with missing personal info                | Item in cart                   | 1. Go to cart  2. Click Checkout  3. Leave fields empty  4. Click Continue                  | Error messages shown under empty required fields                | -              | -      | High     | Major    |
| TC008  | Complete checkout flow (happy path)                        | Valid item in cart             | 1. Add item to cart  2. Checkout  3. Fill info  4. Continue  5. Finish                      | Checkout success message and confirmation page displayed        | -              | -      | High     | Major    |
| TC009  | Validate button label consistency across screens           | Logged in                      | 1. Navigate through inventory, cart, and checkout pages                                     | Buttons follow consistent labeling and placement                | -              | -      | Low      | Minor    |
| TC010  | Edge case – login attempt with SQL-like input              | N/A                            | 1. Enter `' OR '1'='1` in username and password fields  2. Click "Login"                    | Login is blocked, error message shown, no SQL error revealed    | -              | -      | High     | Critical |
