# Negative Test Cases – Shelf Link

Negative testing focuses on invalid inputs and unexpected user behavior to ensure system stability.

---

1. Attempt login with empty username and password  
Expected: Validation messages shown  

2. Create category with only spaces as name  
Expected: Category should not be created  

3. Create product with negative price value  
Expected: Validation error shown  

4. Create product with very large price value  
Expected: System should handle or restrict input  

5. Create product with missing category selection  
Expected: Validation error shown  

6. Use special characters in product name field  
Expected: Input should be sanitized  

7. Attempt to access product page without login  
Expected: Redirect to login page  

8. Refresh page after saving product  
Expected: Data should persist  

9. Rapidly click Save button multiple times  
Expected: No duplicate entries created  

10. Open invalid product ID URL  
Expected: Not found or error page displayed safely  
