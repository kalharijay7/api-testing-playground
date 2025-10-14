# API Basics with Examples

## 📖 What is an API?
An **API (Application Programming Interface)** allows communication between two systems.  
It defines how clients (like browsers or apps) can request data from a server.

---

## 🌐 Types of APIs
- **REST (Representational State Transfer):** Most common, uses HTTP.
- **SOAP:** XML-based, more strict.
- **GraphQL:** Single endpoint, flexible queries.

---

## 🔍 HTTP Methods
| Method | Purpose | Example |
|--------|----------|----------|
| GET | Retrieve data | `/users` |
| POST | Create new data | `/users` |
| PUT | Update existing data | `/users/2` |
| DELETE | Remove data | `/users/2` |

---

## 🧾 Status Codes
| Code | Meaning |
|------|----------|
| 200 | OK |
| 201 | Created |
| 400 | Bad Request |
| 401 | Unauthorized |
| 404 | Not Found |
| 500 | Internal Server Error |

---

## 💡 Example: Using ReqRes API
### 1️⃣ GET Users
**Endpoint:** `https://reqres.in/api/users?page=2`

**Response Example:**
```json
{
  "page": 2,
  "data": [
    {
      "id": 7,
      "email": "michael.lawson@reqres.in"
    }
  ]
}
```

---

## 💡 Example: Using ReqRes API
### 2️⃣ GET Users

**Endpoint:** `https://reqres.in/api/users`

**Body:**
```json
{
  "name": "John",
  "job": "QA Engineer"
}
```
**Response:**
```json
{
  "name": "John",
  "job": "QA Engineer",
  "id": "123",
  "createdAt": "2025-10-13T12:00:00Z"
}
```
---

## 🧠 Summary
- APIs use HTTP methods to perform CRUD operations.
- Postman helps visualize and test API requests easily.
- You can verify responses, status codes, and payloads.

---

## Resources
- [ReqRes API Docs](https://reqres.in/api-docs/)