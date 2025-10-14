# 🧩 API Testing Playground

A hands-on playground for exploring and automating REST APIs using **Postman**, **Newman**, and **Playwright (TypeScript)**.  
This repository documents my journey of mastering **API testing** — from learning fundamentals to building a full-fledged automated test suite.

---

## 🚀 Project Overview

This project is designed to:
- Understand how **REST APIs** work (requests, responses, status codes, etc.)
- Explore **Postman** for manual and semi-automated API testing
- Write and organize **Postman test scripts**
- Run automated tests via **Newman (CLI runner)**
- Transition to **Playwright + TypeScript** for API automation
- Integrate with **GitHub Actions** for CI testing (coming later)

---

## 🗂️ Repository Structure
```
api-testing-playground/
│
├── README.md
├── docs/
│ └── phase1/
│ └── api-basics-with-examples.md # API fundamentals with ReqRes examples
│
├── collections/
│ └── phase1/
│ ├── reqres-playground.postman_collection.json
│ ├── trello-api-auth.postman_collection.json
│ └── environment.postman_environment.json
│
├── reports/
│ └── phase1/
│ └── newman-report.html
│
└── .gitignore
```
---

## 📖 Learning Roadmap

| Week | Focus Area | Tools / Concepts |
|------|-------------|------------------|
| **Week 1** | REST API Basics + Postman Testing | ReqRes API, Trello API, Authorization, Test Scripts |
| **Week 2** | Playwright API Automation Setup | TypeScript, API Assertions, Data-Driven Tests |
| **Week 3** | CI Integration & Reporting | Newman CLI, GitHub Actions, HTML Reports |
| **Week 4** | Advanced Scenarios | Mock APIs, Environment Variables, Chaining Requests |

---

## 🔍 APIs Explored

### 1️⃣ [ReqRes](https://reqres.in)
- Public mock REST API for testing  
- CRUD operations on `/users`  
- Used for learning basic request-response flows

### 2️⃣ [Trello API](https://developer.atlassian.com/cloud/trello/rest/)
- Real API with authentication  
- Demonstrates API Key + Token authorization  
- Used to practice environment variables and chaining requests

---

## 🧠 Concepts Covered

- HTTP methods (GET, POST, PUT, DELETE)
- Status codes (2xx, 4xx, 5xx)
- API Authorization (API Keys, Bearer Tokens)
- Environment and global variables
- Postman test scripts using `pm.expect`
- Chaining requests and data extraction
- Data-driven testing with JSON/CSV files
- Collection runs using **Newman**
- HTML reporting
- Documentation for QA portfolios

---

## 🧪 Example Test Script (Postman)

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response time is less than 500ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});

pm.test("User object contains name", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData).to.have.property("name");
});
```
---
## ⚙️ Running Collections via Newman
You can run any Postman collection from the terminal:

```newman run collections/week1/reqres-playground.postman_collection.json \
  -e collections/week1/environment.postman_environment.json \
  -r cli,html \
  --reporter-html-export reports/week1/newman-report.html
```
---

## 🧾 Reports

All Newman HTML reports are stored under /reports/weekX/.

Example:

Week 1 Report → ReqRes Collection

---
## 🧭 Next Steps

- Complete Postman-based testing for Trello API
- Begin Playwright + TypeScript setup (Week 2)
- Add Newman reports for all collections
- Automate runs using GitHub Actions
- Write portfolio case study (in /docs/)

---
## 🧰 Tech Stack

| Tool | Purpose |
|------|----------|
| **Postman** | Manual & scripted API testing |
| **Newman** | CLI test execution & reporting |
| **Playwright (TypeScript)** | API automation framework |
| **GitHub Actions** | Continuous Integration |
| **Markdown** | Documentation |

---

## 👨‍💻 Author

**Kalhari Jayasinghe**  
QA Engineer | Developer | Test Automation Enthusiast  

🌐 [LinkedIn Profile](https://www.linkedin.com/in/kalharijayasinghe/)  

---

## ⭐ Acknowledgements

- [ReqRes API](https://reqres.in)  
- [Trello REST API](https://developer.atlassian.com/cloud/trello/rest)  
- [Postman Docs](https://learning.postman.com/docs/)  
- [Playwright API Testing Guide](https://playwright.dev/docs/api-testing)

