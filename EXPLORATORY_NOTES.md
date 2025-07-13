# 🔎 Exploratory Testing Report – SauceDemo

**Date:** 2025-06-04  
**Tester:** Julieta Benítez  

## 1. Charter
Explore the core e-commerce flows (login, product discovery, cart, checkout initiation) without a predefined script, aiming to uncover usability issues, UI inconsistencies, and hidden defects.

## 2. Observations
- **Login page**:  
  - Error messages appear one at a time, forcing multiple submissions.  
  - No inline validation hints.

- **Inventory page**:  
  - All products show the same image for `problem_user`—confuses item identification.  
  - Product names and prices are correctly displayed.

- **Cart page**:  
  - Empty cart shows a blank page with no “Your cart is empty” message.  
  - “Remove” and “Checkout” buttons are clear and functional.

- **Checkout form**:  
  - Validation errors shift the layout downward, causing page jump.  
  - Only the first missing field is reported per submission.

## 3. Risks & Areas of Interest
- **Risk:** Users may abandon login if forced to correct fields one by one.  
- **Risk:** Identical images reduce trust and impair easy product selection.  
- **Interest:** Test sorting and filtering in a follow-up exploratory session.  
- **Interest:** Verify responsiveness of cart and checkout flows on mobile.

