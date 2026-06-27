# API Testing — ReqRes.in

**API Under Test:** ReqRes (https://reqres.in) — A hosted REST API for testing  
**Tool Used:** Postman  
**Prepared By:** Siddivinayak Doppalapudi  
**Total Test Cases:** 10  

---

## Base URL

```
https://reqres.in/api
```

---

## API Test Cases

### AT-001 — GET List of Users

| Field | Details |
|---|---|
| **Test ID** | AT-001 |
| **Title** | Fetch list of users from page 2 |
| **Method** | GET |
| **Endpoint** | `/users?page=2` |
| **Headers** | None |
| **Request Body** | None |
| **Expected Status** | 200 OK |
| **Expected Response** | JSON with `data` array containing 6 users, `page` = 2 |
| **Actual Status** | ✅ 200 OK |
| **Status** | PASS |

**Sample Response:**
```json
{
    "page": 2,
    "per_page": 6,
    "total": 12,
    "total_pages": 2,
    "data": [
        {
            "id": 7,
            "email": "michael.lawson@reqres.in",
            "first_name": "Michael",
            "last_name": "Lawson",
            "avatar": "https://reqres.in/img/faces/7-image.jpg"
        },
```

---

### AT-002 — GET Single User (Valid)

| Field | Details |
|---|---|
| **Test ID** | AT-002 |
| **Title** | Fetch a single user by valid ID |
| **Method** | GET |
| **Endpoint** | `/users/2` |
| **Expected Status** | 200 OK |
| **Expected Response** | JSON with `data` object containing user with `id` = 2 |
| **Actual Status** | ✅ 200 OK |
| **Status** | PASS |

---

### AT-003 — GET Single User (Not Found)

| Field | Details |
|---|---|
| **Test ID** | AT-003 |
| **Title** | Fetch user with non-existent ID |
| **Method** | GET |
| **Endpoint** | `/users/999` |
| **Expected Status** | 404 Not Found |
| **Expected Response** | Empty JSON `{}` |
| **Actual Status** | ✅ 404 Not Found |
| **Status** | PASS |
| **Type** | Negative |

---

### AT-004 — POST Create User

| Field | Details |
|---|---|
| **Test ID** | AT-004 |
| **Title** | Create a new user with name and job |
| **Method** | POST |
| **Endpoint** | `/users` |
| **Headers** | `Content-Type: application/json` |
| **Request Body** | `{ "name": "Siddu", "job": "QA Engineer" }` |
| **Expected Status** | 201 Created |
| **Expected Response** | Response contains `id` and `createdAt` fields |
| **Actual Status** | ✅ 201 Created |
| **Status** | PASS |

**Sample Response:**
```json
{
  "name": "Siddu",
  "job": "QA Engineer",
  "id": "123",
  "createdAt": "2026-06-01T10:00:00.000Z"
}
```

---

### AT-005 — POST Create User (Missing Fields)

| Field | Details |
|---|---|
| **Test ID** | AT-005 |
| **Title** | Create user with empty body |
| **Method** | POST |
| **Endpoint** | `/users` |
| **Request Body** | `{}` |
| **Expected Status** | 400 Bad Request |
| **Actual Status** | ❌ 201 Created (ReqRes accepts any payload — known limitation of mock API) |
| **Status** | FAIL (API limitation, not a real bug) |
| **Notes** | ReqRes is a mock API and does not perform real validation |
| **Type** | Negative |

---

### AT-006 — PUT Update User

| Field | Details |
|---|---|
| **Test ID** | AT-006 |
| **Title** | Update user job title using PUT |
| **Method** | PUT |
| **Endpoint** | `/users/2` |
| **Headers** | `Content-Type: application/json` |
| **Request Body** | `{ "name": "Siddu", "job": "Senior QA" }` |
| **Expected Status** | 200 OK |
| **Expected Response** | Response contains `updatedAt` field |
| **Actual Status** | ✅ 200 OK |
| **Status** | PASS |

---

### AT-007 — PATCH Partial Update User

| Field | Details |
|---|---|
| **Test ID** | AT-007 |
| **Title** | Partially update only the job field using PATCH |
| **Method** | PATCH |
| **Endpoint** | `/users/2` |
| **Request Body** | `{ "job": "Lead QA" }` |
| **Expected Status** | 200 OK |
| **Expected Response** | Response contains `updatedAt` |
| **Actual Status** | ✅ 200 OK |
| **Status** | PASS |

---

### AT-008 — DELETE User

| Field | Details |
|---|---|
| **Test ID** | AT-008 |
| **Title** | Delete a user by ID |
| **Method** | DELETE |
| **Endpoint** | `/users/2` |
| **Expected Status** | 204 No Content |
| **Expected Response** | Empty body |
| **Actual Status** | ✅ 204 No Content |
| **Status** | PASS |

---

### AT-009 — POST Register (Successful)

| Field | Details |
|---|---|
| **Test ID** | AT-009 |
| **Title** | Register a user with valid credentials |
| **Method** | POST |
| **Endpoint** | `/register` |
| **Request Body** | `{ "email": "eve.holt@reqres.in", "password": "pistol" }` |
| **Expected Status** | 200 OK |
| **Expected Response** | Response contains `token` |
| **Actual Status** | ✅ 200 OK |
| **Status** | PASS |

---

### AT-010 — POST Register (Missing Password)

| Field | Details |
|---|---|
| **Test ID** | AT-010 |
| **Title** | Register without password field |
| **Method** | POST |
| **Endpoint** | `/register` |
| **Request Body** | `{ "email": "eve.holt@reqres.in" }` |
| **Expected Status** | 400 Bad Request |
| **Expected Response** | `{ "error": "Missing password" }` |
| **Actual Status** | ✅ 400 Bad Request |
| **Status** | PASS |
| **Type** | Negative |

---

## API Testing Summary

| Total | Passed | Failed |
|---|---|---|
| 10 | 9 | 1 (mock API limitation) |

---

## HTTP Status Codes Reference

| Code | Meaning | When to Expect |
|---|---|---|
| 200 | OK | Successful GET, PUT, PATCH |
| 201 | Created | Successful POST |
| 204 | No Content | Successful DELETE |
| 400 | Bad Request | Missing/invalid input |
| 401 | Unauthorized | Missing/invalid auth token |
| 404 | Not Found | Resource doesn't exist |
| 500 | Internal Server Error | Server-side issue |

---
**Attachments:** *<img width="1911" height="924" alt="image" src="https://github.com/user-attachments/assets/3501180e-21e6-4085-9d02-aaf6b7285e5e" />*

*<img width="1892" height="497" alt="image" src="https://github.com/user-attachments/assets/04482708-e8aa-4296-b964-750cc728ae38" />*


