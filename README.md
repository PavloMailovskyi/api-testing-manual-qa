# DummyJSON API – Manual & API Testing Project

##  Overview
This project demonstrates my skills in **manual API testing** using a public mock REST API (DummyJSON).

The project covers:
- Authentication testing
- CRUD operations
- Positive and negative test scenarios
- API validation using Postman scripts
- Test documentation and bug reporting

This project is designed as a **Junior QA / Manual QA portfolio project**.

---

## 🔗 API Under Test
DummyJSON API  
https://dummyjson.com/docs

⚠️ **Important note:**  
DummyJSON is a mock API.  
POST / PUT / PATCH / DELETE requests return simulated responses and do not persist data on the server.  
For this reason, fixed IDs (e.g. `id = 1`) are reused in tests.

---

## 🧪 Testing Scope
- Authentication:
  - Valid login
  - Invalid login
  - Missing required fields
- Products API:
  - Get all products
  - Get product by ID
  - Invalid product ID
  - Create product (positive & negative)
  - Update product (PUT)
  - Partial update (PATCH)
  - Delete product

---

## 🛠 Tools
- Postman
- REST API
- JavaScript (Postman test scripts)
- Markdown
- Git

---

## ▶️ How to Run
1. Import `dummyjson.postman_collection.json` into Postman
2. Create environment variable:
   - `base_url = https://dummyjson.com`
3. Run authentication request to generate token
4. Execute API requests manually or via Collection Runner

---

## 📂 Documentation
- Test Plan – `test-plan.md`
- API Test Cases – `api-test-cases.md`
- Bug Reports – `bug-reports.md`
- Test Data – `test-data.md`
- SQL Checks – `sql-checks.md`
