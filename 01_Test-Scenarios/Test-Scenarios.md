# Test Scenarios – Shelf Link (ESL System)

## Project Overview
Shelf Link is a smart electronic shelf labeling (ESL) platform used for managing products, categories, and price updates in retail environments.

The following test scenarios are designed based on functional requirements and expected system behavior.

---

## Authentication
1. Verify user can log in with valid credentials  
2. Verify user cannot log in with invalid credentials  
3. Verify validation messages appear for empty login fields  
4. Verify user can log out successfully  
5. Verify unauthorized users cannot access protected pages  

---

## Category Management
6. Verify category can be created with valid data  
7. Verify category cannot be created with duplicate name  
8. Verify validation message appears when category name is empty  
9. Verify category can be edited successfully  
10. Verify category deletion behavior when category is linked to products  

---

## Product Management
11. Verify product can be created with valid details  
12. Verify product cannot be created with missing required fields  
13. Verify product price validation for invalid formats  
14. Verify product can be edited successfully  
15. Verify product search and filtering functionality  

---

## ESL Label Update 
16. Verify price update triggers ESL label update  
17. Verify system handles ESL update failure gracefully  

---

## Security & Error Handling
18. Verify system handles invalid URLs safely  
19. Verify application does not crash for unexpected user actions  
20. Verify error messages are clear and user friendly  
