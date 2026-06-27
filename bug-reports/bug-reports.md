# Bug Reports — SauceDemo

**Project:** SauceDemo QA Testing  
**Reported By:** Siddivinayak Doppalapudi  
**Tool Reference:** JIRA (simulated)

---

## BUG-001

| Field | Details |
|---|---|
| **Bug ID** | BUG-001 |
| **Title** | Locked out user receives unhelpful error message with no guidance |
| **Module** | Login |
| **Reported By** | Siddivinayak Doppalapudi |
| **Date** | 2026 |
| **Severity** | Medium |
| **Priority** | Medium |
| **Status** | Open |
| **Environment** | Chrome (latest), Windows 11 |
| **Related TC** | TC-LOGIN-006 |

**Description:**  
When a locked-out user attempts to log in, the application displays a generic error message but does not provide any guidance on what the user should do next (e.g., contact support). This negatively impacts user experience.

**Steps to Reproduce:**  
1. Open https://www.saucedemo.com  
2. Enter username: `locked_out_user`  
3. Enter password: `secret_sauce`  
4. Click the Login button  

**Expected Result:**  
A clear, user-friendly message such as: *"Your account has been locked. Please contact support at support@saucedemo.com."*

**Actual Result:**  
Message displayed: *"Sorry, this user has been locked out."* — No further guidance or contact information provided.

**Attachments:** *(Screenshot to be added)*

---

## BUG-002

| Field | Details |
|---|---|
| **Bug ID** | BUG-002 |
| **Title** | Product sort order resets to default on page refresh |
| **Module** | Inventory |
| **Reported By** | Siddivinayak Doppalapudi |
| **Date** | June 2026 |
| **Severity** | Low |
| **Priority** | Low |
| **Status** | Open |
| **Environment** | Chrome (latest), Windows 11 |
| **Related TC** | TC-INV-005 |

**Description:**  
When a user applies a sort order (e.g., Price: Low to High) and then refreshes the browser, the sort filter resets to the default "Name (A to Z)" without any notification. This can confuse users who expect their filter to persist.

**Steps to Reproduce:**  
1. Log in as `standard_user`  
2. On the inventory page, select sort: "Price (low to high)"  
3. Verify products are sorted by price  
4. Press F5 to refresh the page  

**Expected Result:**  
Sort order is either maintained after refresh, or user is notified that sort was reset.

**Actual Result:**  
Sort silently resets to default with no feedback to the user.

**Attachments:** *(Screenshot to be added)*

---

## BUG-003

| Field | Details |
|---|---|
| **Bug ID** | BUG-003 |
| **Title** | Cart badge count shows stale value briefly after removing item from cart page |
| **Module** | Shopping Cart |
| **Reported By** | Siddivinayak Doppalapudi |
| **Date** | June 2026 |
| **Severity** | Medium |
| **Priority** | Medium |
| **Status** | Open |
| **Environment** | Chrome (latest), Windows 11 |
| **Related TC** | TC-CART-004 |

**Description:**  
After removing an item from the cart page, the cart badge in the top-right header does not update immediately — it briefly shows the old count before correcting itself. This creates a momentary inconsistency in the UI.

**Steps to Reproduce:**  
1. Log in as `standard_user`  
2. Add 2 products to the cart  
3. Navigate to the cart page  
4. Click "Remove" on one item  
5. Immediately observe the cart badge in the header  

**Expected Result:**  
Cart badge should instantly update to reflect the new item count (1).

**Actual Result:**  
Badge briefly shows "2" before updating to "1".

**Attachments:** *(Screenshot/screen recording to be added)*

---

## BUG-004

| Field | Details |
|---|---|
| **Bug ID** | BUG-004 |
| **Title** | Checkout form accepts empty First Name field and proceeds to next step |
| **Module** | Checkout |
| **Reported By** | Siddivinayak Doppalapudi |
| **Date** | June 2026 |
| **Severity** | High |
| **Priority** | High |
| **Status** | Open |
| **Environment** | Chrome (latest), Windows 11 |
| **Related TC** | TC-CHK-003 |

**Description:**  
The checkout form does not validate the First Name field. When the field is left empty and the user clicks "Continue", the form proceeds to the next step instead of displaying a validation error. This is a data integrity issue.

**Steps to Reproduce:**  
1. Log in as `standard_user`  
2. Add any item to cart  
3. Go to cart and click "Checkout"  
4. Leave **First Name** blank  
5. Fill in Last Name: `Doe`  
6. Fill in Zip: `380015`  
7. Click "Continue"  

**Expected Result:**  
Validation error: *"First Name is required"*

**Actual Result:**  
Form proceeds to Checkout Overview with no error.

**Severity Justification:**  
This is a High severity bug because it allows incomplete customer data to pass through a business-critical checkout flow, which could cause issues with order fulfillment.

**Attachments:** *(Screenshot to be added)*

---

## BUG-005

| Field | Details |
|---|---|
| **Bug ID** | BUG-005 |
| **Title** | Product images broken / incorrect for performance_glitch_user |
| **Module** | Inventory |
| **Reported By** | Siddivinayak Doppalapudi |
| **Date** | June 2026 |
| **Severity** | High |
| **Priority** | High |
| **Status** | Open |
| **Environment** | Chrome (latest), Windows 11 |
| **Related TC** | N/A |

**Description:**  
When logged in as `performance_glitch_user`, some product images on the inventory page fail to load correctly or display the wrong image for a product. This is a visual regression bug that breaks the user experience.

**Steps to Reproduce:**  
1. Open https://www.saucedemo.com  
2. Log in with username: `performance_glitch_user`, password: `secret_sauce`  
3. Observe the product images on the inventory page  

**Expected Result:**  
All product images load correctly and match their respective product names.

**Actual Result:**  
One or more product images are broken or mismatched.

**Severity Justification:**  
High severity because broken/incorrect product images directly impact the ability of a user to make a purchase decision — a core business function.

**Attachments:** *(Screenshot to be added)*
