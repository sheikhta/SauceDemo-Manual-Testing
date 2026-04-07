# 🐞 Bug Reports – SauceDemo (Manual Web Testing)

## 📌 Project
**SauceDemo – Manual QA Web Testing**

---

## 🐞 BUG-01 – Cart does not allow adding more than one unit of the same product

**Type:** Functional / Usability  
**Severity:** Medium  
**Priority:** Low–Medium  

### Preconditions
- User logged in with `standard_user`
- User on Products page

### Steps to Reproduce
1. Log in to the application.
2. Click **Add to Cart** on any product.
3. Attempt to add the same product again.
4. Open the Cart page.

### Expected Result
- User should be able to add multiple units of the same product  
  **OR**
- The UI should clearly indicate that only one unit per product is allowed.

### Actual Result
- The **Add to Cart** button changes to **Remove**.
- No option to increase quantity is available.
- No message explains the limitation.
- Cart shows only one unit of the product.

### Impact
- May confuse users expecting standard e-commerce behavior.
- Lack of feedback reduces usability.

### Evidence
- N/A (functional limitation observed during execution)

---

## 🐞 BUG-02 – Checkout validation fails only when application enters inconsistent state (intermittent)

**Type:** Functional  
**Severity:** Medium–High  
**Priority:** Medium  
**Reproducibility:** Intermittent — occurs only after UI/cart state becomes inconsistent.

### Preconditions
- User logged in
- Application already shows inconsistent behavior (e.g., Add to Cart buttons not responding or product state incorrect)
- At least one navigation between Products, Cart, and Checkout pages

### Steps to Reproduce
1. Log in with `standard_user`.
2. Interact with the application until UI state becomes inconsistent (e.g., some Add to Cart buttons stop responding).
3. Add at least one product to the cart (if possible).
4. Navigate to Cart.
5. Click **Checkout**.
6. Leave required fields incomplete.
7. Click **Continue**.

### Expected Result
- Validation MUST stop the user from continuing.
- Error message should inform which fields are missing.

### Actual Result
- When the application is already in an inconsistent state,  
  the Checkout page **sometimes allows continuation with incomplete fields**.
- This does NOT occur when the application is functioning correctly.

### Impact
- Validation logic can break under certain UI/cart state conditions.
- This indicates deeper issues with state management.
- In a real product, this could lead to invalid orders or corrupted checkout flow.

### Evidence
- Pending (intermittent issue)

---

## 🐞 BUG-03 – Intermittent loss of Add to Cart button functionality after navigation and checkout attempt

**Type:** Functional / UI / State Management  
**Severity:** High  
**Priority:** Medium  
**Reproducibility:** Intermittent  

### Preconditions
- User logged in
- Multiple navigations between Products, Product Detail, Cart, and Checkout pages

### Steps to Reproduce
1. Log in with `standard_user`.
2. Add one or more products to the cart.
3. Navigate repeatedly between:
   - Products page  
   - Product detail page  
   - Cart page  
4. Go to Checkout.
5. Attempt to continue checkout with incomplete fields.
6. Navigate back to Products page.
7. Try clicking **Add to Cart** on different products.

### Expected Result
- Checkout should enforce required field validation.
- All **Add to Cart** buttons should remain functional.
- Product state should remain consistent.

### Actual Result
- Some **Add to Cart** buttons become unresponsive.
- Products already in the cart can still be removed and re-added.
- Behavior resets after refresh or re-login.

### Impact
- Users cannot add certain products.
- Inconsistent UI behavior.
- Loss of trust in application stability.

### Evidence
- Pending (intermittent behavior difficult to capture)