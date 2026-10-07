# Day 02 - Test Design Notes (Sauce Demo)

## 1. Test Design Techniques Applied

### A. Equivalence Partitioning (EP) - Login Credentials
- **Valid Partition:** `standard_user`, `problem_user`, `performance_glitch_user`, `error_user`, `visual_user` with password `secret_sauce`.
- **Invalid Partition (Username):** Unregistered username (e.g., `invalid_user`), blank username.
- **Invalid Partition (Password):** Incorrect password (e.g., `wrong_pass`), blank password.
- **Locked-out Partition:** `locked_out_user` with `secret_sauce` (valid credentials, restricted account status).

### B. Boundary Value Analysis (BVA) - Checkout Form Fields
Field: First Name, Last Name, Postal Code
- **Min - 1 (Invalid):** 0 characters (Empty field submit)
- **Min (Valid):** 1 character (e.g., "A")
- **Nominal (Valid):** Standard input length (e.g., "John")
- **Max / Extreme (Valid/Stress):** Long string input (e.g., 100+ characters)

---

## 2. Test Execution Scenarios Identified

1. **Login Module:**
   - Successful login with standard user.
   - Prevent login with empty username/password.
   - Verify locked-out user receives specific error banner.
2. **Product Catalog & Cart:**
   - Verify sorting functional order (A-Z, Z-A, Price Low-High, Price High-Low).
   - Verify badge count updates when adding/removing items from inventory page and detail page.
3. **Checkout Flow:**
   - Complete checkout with valid inputs.
   - Trigger field validations on missing First Name, Last Name, or Zip Code.
