# Test Data

## Authentication
Valid:
- username: emilys
- password: emilyspass

Invalid:
- username: wronguser
- password: wrongpassword

---

## Products
Valid product:
```json
{
  "title": "QA Test Product",
  "price": 100
}
 ```
Invalid Product:
```json
{
  "title": "QA Test Product",
  "price": -100
}
```