# Test Plan — SauceDemo Web Application

**Project:** SauceDemo E-Commerce Web App  
**Version:** 1.0   

---

## 1. Introduction

This test plan describes the testing strategy, scope, objectives, and approach for manual testing of the SauceDemo web application (https://www.saucedemo.com). SauceDemo is a demo e-commerce site that simulates a real-world shopping application.

---

## 2. Objectives

- Verify that all major functionalities work as expected
- Identify and document defects with clear reproduction steps
- Ensure the application provides a seamless user experience
- Validate business-critical flows: login → browse → cart → checkout

---

## 3. Scope

### In Scope
- Login and Authentication
- Product Inventory Listing and Sorting
- Shopping Cart (add, remove, count)
- Checkout Flow (personal info, order summary, confirmation)
- API Testing (ReqRes public API as a supplementary exercise)

### Out of Scope
- Performance / Load Testing
- Mobile Responsiveness
- Backend / Database Testing
- Payment Gateway (not present in SauceDemo)

---

## 4. Test Approach

### Testing Types Applied
| Type | Description |
|---|---|
| Functional Testing | Verify each feature works per expected behavior |
| Smoke Testing | Quick sanity check — can user log in and reach inventory? |
| Sanity Testing | After a bug fix, verify that specific fix works |
| Regression Testing | After changes, re-verify all previously passing test cases |
| Negative Testing | Input invalid data to verify proper error handling |
| End-to-End Testing | Full flow from login to order completion |
| API Testing | REST API tests using ReqRes.in with Postman |

### Test Design Techniques
- **Equivalence Partitioning** — Divide inputs into valid/invalid classes
- **Boundary Value Analysis** — Test at min/max limits of input fields
- **Decision Table** — Test all combinations of login credentials
- **Error Guessing** — Test areas likely to have bugs based on experience

---

## 5. Test Environment

| Parameter | Details |
|---|---|
| Application URL | https://www.saucedemo.com |
| Browser | Google Chrome (latest) |
| OS | Windows 11 |
| API Tool | Postman |
| Bug Tracking | JIRA (simulated as Markdown reports) |

### Test Accounts Available in SauceDemo
| Username | Password | Type |
|---|---|---|
| standard_user | secret_sauce | Normal valid user |
| locked_out_user | secret_sauce | Locked account |
| problem_user | secret_sauce | User with UI bugs |
| performance_glitch_user | secret_sauce | Slow loading user |
| error_user | secret_sauce | Error-prone user |
| visual_user | secret_sauce | Visual bug user |

---

## 6. Entry and Exit Criteria

### Entry Criteria (when to start testing)
- Application is accessible at the URL
- Test cases are reviewed and ready
- Test environment (browser, Postman) is set up

### Exit Criteria (when to stop testing)
- All planned test cases executed
- All High/Critical bugs are reported
- Test summary report is prepared

---

## 7. Test Deliverables

- ✅ Test Plan (this document)
- ✅ Manual Test Cases (per module)
- ✅ Bug Reports (JIRA-style)
- ✅ API Test Cases + Postman Collection
- ✅ Test Execution Summary (in README)

---

| Role | Name |
|---|---|
| Test Engineer | Siddivinayak Doppalapudi |
| Application Under Test | SauceDemo (Sauce Labs) |
