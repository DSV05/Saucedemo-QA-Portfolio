# Test Cases — Shopping Cart Module

**Module:** Shopping Cart  
**Application:** SauceDemo (https://www.saucedemo.com)  
**Prepared By:** Siddivinayak Doppalapudi  
**Total Test Cases:** 7  
**Precondition for all:** User is logged in as `standard_user`

---

### TC-CART-001
| Field | Details |
|---|---|
| **Test Case ID** | TC-CART-001 |
| **Title** | Add single item to cart |
| **Test Steps** | 1. Click "Add to cart" on any product |
| **Expected Result** | Item added, cart badge shows 1, button changes to "Remove" |
| **Actual Result** | ✅ Works as expected |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Functional |

---

### TC-CART-002
| Field | Details |
|---|---|
| **Test Case ID** | TC-CART-002 |
| **Title** | Add multiple items to cart |
| **Test Steps** | 1. Click "Add to cart" on 3 different products |
| **Expected Result** | Cart badge shows 3 |
| **Actual Result** | ✅ Badge shows correct count |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Functional |

---

### TC-CART-003
| Field | Details |
|---|---|
| **Test Case ID** | TC-CART-003 |
| **Title** | Remove item from cart via inventory page |
| **Test Steps** | 1. Add a product to cart <br> 2. Click "Remove" on the same product |
| **Expected Result** | Item removed, cart badge decreases by 1, button reverts to "Add to cart" |
| **Actual Result** | ✅ Works as expected |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Functional |

---

### TC-CART-004
| Field | Details |
|---|---|
| **Test Case ID** | TC-CART-004 |
| **Title** | Cart badge does not update immediately after remove (edge case) |
| **Test Steps** | 1. Add 2 items to cart <br> 2. Open cart page <br> 3. Remove one item from cart page <br> 4. Observe badge |
| **Expected Result** | Badge should immediately update to 1 |
| **Actual Result** | ❌ Badge shows stale count briefly before refreshing |
| **Status** | FAIL |
| **Priority** | Medium |
| **Type** | Functional / UI |
| **Bug Ref** | BUG-003 |

---

### TC-CART-005
| Field | Details |
|---|---|
| **Test Case ID** | TC-CART-005 |
| **Title** | Cart persists items after navigating back to inventory |
| **Test Steps** | 1. Add 2 items to cart <br> 2. Click "Continue Shopping" <br> 3. Return to inventory |
| **Expected Result** | Cart still shows 2 items |
| **Actual Result** | ✅ Cart persisted |
| **Status** | PASS |
| **Priority** | Medium |
| **Type** | Functional |

---

### TC-CART-006
| Field | Details |
|---|---|
| **Test Case ID** | TC-CART-006 |
| **Title** | Cart page shows correct product details |
| **Test Steps** | 1. Add a product to cart <br> 2. Open cart page |
| **Expected Result** | Product name, description, price, and quantity shown correctly |
| **Actual Result** | ✅ All details correct |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Functional |

---

### TC-CART-007
| Field | Details |
|---|---|
| **Test Case ID** | TC-CART-007 |
| **Title** | Empty cart shows no items and checkout button is still present |
| **Test Steps** | 1. Go to cart without adding any items |
| **Expected Result** | Cart is empty, but Checkout button is still accessible |
| **Actual Result** | ✅ Empty cart shown, button present |
| **Status** | PASS |
| **Priority** | Low |
| **Type** | Edge Case |

---

## Summary

| Total | Passed | Failed |
|---|---|---|
| 7 | 6 | 1 |
