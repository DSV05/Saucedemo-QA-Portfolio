# Test Cases — Inventory / Product Listing Module

**Module:** Product Inventory  
**Application:** SauceDemo (https://www.saucedemo.com)  
**Prepared By:** Siddivinayak Doppalapudi  
**Total Test Cases:** 8  
**Precondition for all:** User is logged in as `standard_user`

---

### TC-INV-001
| Field | Details |
|---|---|
| **Test Case ID** | TC-INV-001 |
| **Title** | Inventory page loads with products after login |
| **Test Steps** | 1. Log in with valid credentials <br> 2. Observe the inventory page |
| **Expected Result** | 6 products are displayed with name, image, description, and price |
| **Actual Result** | ✅ All 6 products displayed correctly |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Smoke / Functional |

---

### TC-INV-002
| Field | Details |
|---|---|
| **Test Case ID** | TC-INV-002 |
| **Title** | Sort products by Price (Low to High) |
| **Test Steps** | 1. Click the sort dropdown <br> 2. Select "Price (low to high)" |
| **Expected Result** | Products reorder from lowest to highest price |
| **Actual Result** | ✅ Products sorted correctly |
| **Status** | PASS |
| **Priority** | Medium |
| **Type** | Functional |

---

### TC-INV-003
| Field | Details |
|---|---|
| **Test Case ID** | TC-INV-003 |
| **Title** | Sort products by Price (High to Low) |
| **Test Steps** | 1. Click the sort dropdown <br> 2. Select "Price (high to low)" |
| **Expected Result** | Products reorder from highest to lowest price |
| **Actual Result** | ✅ Products sorted correctly |
| **Status** | PASS |
| **Priority** | Medium |
| **Type** | Functional |

---

### TC-INV-004
| Field | Details |
|---|---|
| **Test Case ID** | TC-INV-004 |
| **Title** | Sort products by Name (A to Z) |
| **Test Steps** | 1. Click the sort dropdown <br> 2. Select "Name (A to Z)" |
| **Expected Result** | Products sorted alphabetically A→Z |
| **Actual Result** | ✅ Sorted correctly |
| **Status** | PASS |
| **Priority** | Low |
| **Type** | Functional |

---

### TC-INV-005
| Field | Details |
|---|---|
| **Test Case ID** | TC-INV-005 |
| **Title** | Sort order resets after page refresh |
| **Test Steps** | 1. Sort by "Price (low to high)" <br> 2. Refresh the browser |
| **Expected Result** | Sort order should persist or reset to default (either is acceptable UX) |
| **Actual Result** | ❌ Sort resets to default but no user notification |
| **Status** | FAIL |
| **Priority** | Low |
| **Type** | Functional / UX |
| **Bug Ref** | BUG-002 |

---

### TC-INV-006
| Field | Details |
|---|---|
| **Test Case ID** | TC-INV-006 |
| **Title** | Click on product name navigates to product detail page |
| **Test Steps** | 1. Click on any product name |
| **Expected Result** | Product detail page opens with full description and price |
| **Actual Result** | ✅ Product detail page opened |
| **Status** | PASS |
| **Priority** | Medium |
| **Type** | Functional |

---

### TC-INV-007
| Field | Details |
|---|---|
| **Test Case ID** | TC-INV-007 |
| **Title** | Add to cart button visible on each product |
| **Test Steps** | 1. View the inventory page |
| **Expected Result** | Every product card has an "Add to cart" button |
| **Actual Result** | ✅ All products have the button |
| **Status** | PASS |
| **Priority** | High |
| **Type** | UI / Functional |

---

### TC-INV-008
| Field | Details |
|---|---|
| **Test Case ID** | TC-INV-008 |
| **Title** | Add to cart from inventory page updates cart badge |
| **Test Steps** | 1. Click "Add to cart" on any product <br> 2. Observe the cart icon (top right) |
| **Expected Result** | Cart badge shows count = 1 |
| **Actual Result** | ✅ Badge updated to 1 |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Functional |

---

## Summary

| Total | Passed | Failed |
|---|---|---|
| 8 | 7 | 1 |
