# Test Cases — Checkout Module

**Module:** Checkout Flow  
**Application:** SauceDemo (https://www.saucedemo.com)  
**Prepared By:** Siddivinayak Doppalapudi  
**Total Test Cases:** 10  
**Precondition for all:** User logged in as `standard_user` with at least 1 item in cart

---

### TC-CHK-001
| Field | Details |
|---|---|
| **Test Case ID** | TC-CHK-001 |
| **Title** | Checkout button navigates to checkout step 1 |
| **Test Steps** | 1. Add item to cart <br> 2. Go to cart <br> 3. Click "Checkout" |
| **Expected Result** | User is taken to "Checkout: Your Information" page |
| **Actual Result** | ✅ Navigated to checkout step 1 |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Functional |

---

### TC-CHK-002
| Field | Details |
|---|---|
| **Test Case ID** | TC-CHK-002 |
| **Title** | Complete checkout with valid information |
| **Test Steps** | 1. Enter First Name: `John` <br> 2. Enter Last Name: `Doe` <br> 3. Enter Zip: `380015` <br> 4. Click Continue |
| **Expected Result** | Navigated to "Checkout: Overview" page |
| **Actual Result** | ✅ Moved to overview page |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Functional / E2E |

---

### TC-CHK-003
| Field | Details |
|---|---|
| **Test Case ID** | TC-CHK-003 |
| **Title** | Checkout with empty First Name |
| **Test Steps** | 1. Leave First Name empty <br> 2. Fill Last Name and Zip <br> 3. Click Continue |
| **Expected Result** | Error: "First Name is required" |
| **Actual Result** | ❌ Form submits without error, proceeds to next step |
| **Status** | FAIL |
| **Priority** | High |
| **Type** | Negative / Validation |
| **Bug Ref** | BUG-004 |

---

### TC-CHK-004
| Field | Details |
|---|---|
| **Test Case ID** | TC-CHK-004 |
| **Title** | Checkout with empty Last Name |
| **Test Steps** | 1. Fill First Name <br> 2. Leave Last Name empty <br> 3. Fill Zip <br> 4. Click Continue |
| **Expected Result** | Error: "Last Name is required" |
| **Actual Result** | ✅ Error shown |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Negative |

---

### TC-CHK-005
| Field | Details |
|---|---|
| **Test Case ID** | TC-CHK-005 |
| **Title** | Checkout with empty Zip code |
| **Test Steps** | 1. Fill First Name and Last Name <br> 2. Leave Zip empty <br> 3. Click Continue |
| **Expected Result** | Error: "Postal Code is required" |
| **Actual Result** | ✅ Error shown |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Negative |

---

### TC-CHK-006
| Field | Details |
|---|---|
| **Test Case ID** | TC-CHK-006 |
| **Title** | Order overview shows correct product, price, and tax |
| **Test Steps** | 1. Complete checkout step 1 <br> 2. View overview page |
| **Expected Result** | Product name, quantity, item price, tax, and total shown correctly |
| **Actual Result** | ✅ All values correct |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Functional |

---

### TC-CHK-007
| Field | Details |
|---|---|
| **Test Case ID** | TC-CHK-007 |
| **Title** | Finish button completes the order |
| **Test Steps** | 1. Complete overview page <br> 2. Click "Finish" |
| **Expected Result** | Order confirmation page shown with "Thank you" message |
| **Actual Result** | ✅ Confirmation page displayed |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Functional / E2E |

---

### TC-CHK-008
| Field | Details |
|---|---|
| **Test Case ID** | TC-CHK-008 |
| **Title** | Cart is empty after order completion |
| **Test Steps** | 1. Complete checkout fully <br> 2. Check cart icon badge |
| **Expected Result** | Cart badge disappears (empty cart) |
| **Actual Result** | ✅ Cart cleared after order |
| **Status** | PASS |
| **Priority** | Medium |
| **Type** | Functional |

---

### TC-CHK-009
| Field | Details |
|---|---|
| **Test Case ID** | TC-CHK-009 |
| **Title** | Cancel button on checkout step 1 returns to cart |
| **Test Steps** | 1. Click "Checkout" from cart <br> 2. Click "Cancel" on step 1 |
| **Expected Result** | User returned to cart page |
| **Actual Result** | ✅ Returned to cart |
| **Status** | PASS |
| **Priority** | Medium |
| **Type** | Functional |

---

### TC-CHK-010
| Field | Details |
|---|---|
| **Test Case ID** | TC-CHK-010 |
| **Title** | Back Home button after order confirmation returns to inventory |
| **Test Steps** | 1. Complete order <br> 2. Click "Back Home" button on confirmation page |
| **Expected Result** | User redirected to inventory page |
| **Actual Result** | ✅ Redirected to inventory |
| **Status** | PASS |
| **Priority** | Low |
| **Type** | Functional |

---

## Summary

| Total | Passed | Failed |
|---|---|---|
| 10 | 9 | 1 |
