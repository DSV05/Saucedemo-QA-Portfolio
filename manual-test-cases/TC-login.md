# Test Cases — Login Module

**Module:** Login / Authentication  
**Application:** SauceDemo (https://www.saucedemo.com)  
**Prepared By:** Siddivinayak Doppalapudi  
**Total Test Cases:** 12  

---

## Test Cases

### TC-LOGIN-001
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-001 |
| **Title** | Valid login with standard_user |
| **Preconditions** | Browser open, SauceDemo URL loaded |
| **Test Steps** | 1. Enter username: `standard_user` <br> 2. Enter password: `secret_sauce` <br> 3. Click Login button |
| **Expected Result** | User is redirected to the inventory/products page |
| **Actual Result** | ✅ Redirected to inventory page |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Positive / Functional |

---

### TC-LOGIN-002
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-002 |
| **Title** | Login with incorrect password |
| **Preconditions** | Browser open, SauceDemo URL loaded |
| **Test Steps** | 1. Enter username: `standard_user` <br> 2. Enter password: `wrongpassword` <br> 3. Click Login button |
| **Expected Result** | Error message displayed: "Username and password do not match" |
| **Actual Result** | ✅ Error message shown |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Negative |

---

### TC-LOGIN-003
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-003 |
| **Title** | Login with empty username and password |
| **Preconditions** | Browser open, SauceDemo URL loaded |
| **Test Steps** | 1. Leave both fields empty <br> 2. Click Login button |
| **Expected Result** | Error message: "Username is required" |
| **Actual Result** | ✅ Error message shown |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Negative / Boundary |

---

### TC-LOGIN-004
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-004 |
| **Title** | Login with empty username only |
| **Preconditions** | Browser open, SauceDemo URL loaded |
| **Test Steps** | 1. Leave username empty <br> 2. Enter password: `secret_sauce` <br> 3. Click Login |
| **Expected Result** | Error: "Username is required" |
| **Actual Result** | ✅ Error message shown |
| **Status** | PASS |
| **Priority** | Medium |
| **Type** | Negative |

---

### TC-LOGIN-005
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-005 |
| **Title** | Login with empty password only |
| **Preconditions** | Browser open, SauceDemo URL loaded |
| **Test Steps** | 1. Enter username: `standard_user` <br> 2. Leave password empty <br> 3. Click Login |
| **Expected Result** | Error: "Password is required" |
| **Actual Result** | ✅ Error message shown |
| **Status** | PASS |
| **Priority** | Medium |
| **Type** | Negative |

---

### TC-LOGIN-006
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-006 |
| **Title** | Login with locked_out_user account |
| **Preconditions** | Browser open, SauceDemo URL loaded |
| **Test Steps** | 1. Enter username: `locked_out_user` <br> 2. Enter password: `secret_sauce` <br> 3. Click Login |
| **Expected Result** | Clear error message explaining account is locked |
| **Actual Result** | ❌ Error shown but message is not user-friendly (no guidance given) |
| **Status** | FAIL |
| **Priority** | Medium |
| **Type** | Negative |
| **Bug Ref** | BUG-001 |

---

### TC-LOGIN-007
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-007 |
| **Title** | Password field masks input |
| **Preconditions** | Browser open, SauceDemo URL loaded |
| **Test Steps** | 1. Click on the password field <br> 2. Type any characters |
| **Expected Result** | Characters appear as dots/asterisks (masked) |
| **Actual Result** | ✅ Password is masked |
| **Status** | PASS |
| **Priority** | Medium |
| **Type** | Functional / Security |

---

### TC-LOGIN-008
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-008 |
| **Title** | Login with username in all caps (case sensitivity) |
| **Preconditions** | Browser open, SauceDemo URL loaded |
| **Test Steps** | 1. Enter username: `STANDARD_USER` <br> 2. Enter password: `secret_sauce` <br> 3. Click Login |
| **Expected Result** | Login fails (username is case-sensitive) |
| **Actual Result** | ✅ Login failed with error message |
| **Status** | PASS |
| **Priority** | Low |
| **Type** | Negative / Boundary |

---

### TC-LOGIN-009
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-009 |
| **Title** | Successful logout after login |
| **Preconditions** | User is logged in as standard_user |
| **Test Steps** | 1. Click the hamburger menu (top left) <br> 2. Click "Logout" |
| **Expected Result** | User is redirected back to the login page |
| **Actual Result** | ✅ Redirected to login page |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Functional |

---

### TC-LOGIN-010
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-010 |
| **Title** | Access inventory page without login (direct URL) |
| **Preconditions** | User is NOT logged in |
| **Test Steps** | 1. Open browser <br> 2. Navigate directly to `https://www.saucedemo.com/inventory.html` |
| **Expected Result** | User is redirected to login page |
| **Actual Result** | ✅ Redirected to login page |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Security / Negative |

---

### TC-LOGIN-011
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-011 |
| **Title** | Login with SQL injection in username field |
| **Preconditions** | Browser open, SauceDemo URL loaded |
| **Test Steps** | 1. Enter username: `' OR '1'='1` <br> 2. Enter password: `anything` <br> 3. Click Login |
| **Expected Result** | Login fails, no unauthorized access |
| **Actual Result** | ✅ Login failed |
| **Status** | PASS |
| **Priority** | High |
| **Type** | Security / Negative |

---

### TC-LOGIN-012
| Field | Details |
|---|---|
| **Test Case ID** | TC-LOGIN-012 |
| **Title** | Error message disappears after correcting credentials |
| **Preconditions** | Error message is visible after a failed login |
| **Test Steps** | 1. Trigger a login error <br> 2. Click the X icon on the error message |
| **Expected Result** | Error message is dismissed |
| **Actual Result** | ✅ Error dismissed |
| **Status** | PASS |
| **Priority** | Low |
| **Type** | Functional / UI |

---

## Summary

| Total | Passed | Failed |
|---|---|---|
| 12 | 11 | 1 |
