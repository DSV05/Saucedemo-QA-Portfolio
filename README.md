# 🧪 SauceDemo QA Portfolio

A complete manual QA testing project for [SauceDemo](https://www.saucedemo.com) — a demo e-commerce web application built for testing practice.

This project demonstrates end-to-end QA skills including test planning, test case design, bug reporting, and API testing.

---

## 📁 Project Structure

```
saucedemo-qa-portfolio/
│
├── test-plan/
│   └── test-plan.md               # Overall testing strategy and scope
│
├── manual-test-cases/
│   ├── TC-login.md                # Login module test cases
│   ├── TC-inventory.md            # Product listing & sorting test cases
│   ├── TC-cart.md                 # Cart functionality test cases
│   └── TC-checkout.md             # Checkout flow test cases
│
├── bug-reports/
│   ├── BUG-001.md                 # Locked out user shows no clear error
│   ├── BUG-002.md                 # Sort order resets on page refresh
│   ├── BUG-003.md                 # Cart badge count not updating
│   ├── BUG-004.md                 # Checkout allows empty first name
│   └── BUG-005.md                 # Product image broken for glitch user
│
├── api-testing/
│   ├── reqres-api-tests.md        # Manual API test cases (ReqRes API)
│   └── postman-collection.json    # Importable Postman collection
│
└── README.md                      # This file
```

---

## 🎯 Scope of Testing

| Module | Type of Testing |
|---|---|
| Login | Functional, Negative, Boundary |
| Product Inventory | Functional, UI |
| Shopping Cart | Functional, Edge Cases |
| Checkout Flow | Functional, Negative, End-to-End |
| API (ReqRes) | API Testing (GET, POST, PUT, DELETE) |

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| [SauceDemo](https://www.saucedemo.com) | Application under test |
| [ReqRes](https://reqres.in) | REST API for API testing practice |
| Postman | API test execution and collection |
| JIRA (simulated) | Bug tracking (reports documented here) |
| Markdown | Documentation |

---

## 🧠 Testing Techniques Applied

- **Equivalence Partitioning** — Grouping valid/invalid login inputs
- **Boundary Value Analysis** — Min/max character inputs for form fields
- **Decision Table Testing** — Login combinations (valid user + valid/invalid password)
- **End-to-End Testing** — Full checkout flow from login to order confirmation
- **Negative Testing** — Empty fields, wrong credentials, invalid data

---

## 🐛 Bugs Found

| Bug ID | Title | Severity | Status |
|---|---|---|---|
| BUG-001 | Locked user gets no meaningful error message | Medium | Open |
| BUG-002 | Sort order resets on browser refresh | Low | Open |
| BUG-003 | Cart badge doesn't update after remove | Medium | Open |
| BUG-004 | Checkout accepts empty First Name field | High | Open |
| BUG-005 | Product images broken for glitch_user | High | Open |

---

## 📊 Test Execution Summary

| Module | Total TCs | Passed | Failed | Blocked |
|---|---|---|---|---|
| Login | 12 | 10 | 2 | 0 |
| Inventory | 8 | 7 | 1 | 0 |
| Cart | 7 | 6 | 1 | 0 |
| Checkout | 10 | 8 | 2 | 0 |
| **Total** | **37** | **31** | **6** | **0** |

---

## 👨‍💻 About Me

**Siddivinayak Doppalapudi**  
B.Tech Computer Engineering (AI), Ganpat University  
Data Analyst Intern @ IQAC, Ganpat University

🔗 [Portfolio](https://dsv05.github.io/Portfolio1) | [LinkedIn](https://linkedin.com/in/doppalapudisiddivinayak)

---

## 📌 How to Use This Project

1. Browse `test-plan/` to understand the overall testing approach
2. Check `manual-test-cases/` for detailed test case documentation
3. See `bug-reports/` for sample JIRA-style defect reports
4. Import `api-testing/postman-collection.json` into Postman to run API tests
