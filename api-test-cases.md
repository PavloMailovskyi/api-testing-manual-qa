# API Test Cases – DummyJSON

## Authentication

TC-01 Valid Login  
Endpoint: POST /auth/login  
Expected: 200 OK, token returned

TC-02 Invalid Login  
Endpoint: POST /auth/login  
Expected: 400 Bad Request

TC-03 Missing Required Fields  
Endpoint: POST /auth/login  
Expected: 400 Bad Request

---

## Products

TC-04 Get All Products  
Endpoint: GET /products  
Expected: 200 OK

TC-05 Get Product by ID  
Endpoint: GET /products/1  
Expected: 200 OK

TC-06 Get Product with Invalid ID  
Endpoint: GET /products/9999  
Expected: 404 Not Found

TC-07 Create Product  
Endpoint: POST /products/add  
Expected: 200 / 201

TC-08 Create Product with Negative Price  
Endpoint: POST /products/add  
Expected: Validation error (observed: accepted)

TC-09 Update Product (PUT)  
Endpoint: PUT /products/1  
Expected: 200 OK

TC-10 Partial Update Product (PATCH)  
Endpoint: PATCH /products/1  
Expected: 200 OK

TC-11 Delete Product  
Endpoint: DELETE /products/1  
Expected: 200 OK
