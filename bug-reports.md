## BR-01 Negative Price Accepted
Endpoint: POST /products/add  
Severity: Medium  

Description:  
API allows creation of a product with negative price value.

Expected Result:  
Validation error returned.

Actual Result:  
Product is accepted and returned in response