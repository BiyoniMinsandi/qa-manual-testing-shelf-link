# Test Cases – Shelf Link (Manual Testing)

## Note
Login functionality was not working during execution.  
Affected test cases are marked as **Blocked** or **Not Executed** due to environment limitations.

---

| Test Case ID | Title | Preconditions | Steps | Expected Result | Actual Result | Status | Remarks |
|-------------|------|--------------|------|----------------|--------------|--------|--------|

| SL-TC-01 | Login with valid credentials | User account exists | Enter valid username and password → Click Login | User should be logged in | Login not successful | Blocked | Login functionality not working |

| SL-TC-02 | Login with invalid password | User account exists | Enter valid username and wrong password → Login | Error message displayed | Not executed | Blocked | Blocked due to login issue |

| SL-TC-03 | Login with empty fields | None | Click Login without entering credentials | Validation messages shown | Not executed | Blocked | Blocked due to login issue |

| SL-TC-04 | Logout from application | User logged in | Click Logout | User logged out successfully | Not executed | Not Executed | Blocked due to login issue |

| SL-TC-05 | Access protected page without login | None | Open product page URL directly | Redirect to login | Not executed | Not Executed | Login unavailable |

---

## Category Module

| SL-TC-06 | Create category with valid name | User logged in | Add category with valid name | Category created | Not executed | Not Executed | Login blocked |

| SL-TC-07 | Create category with empty name | User logged in | Click Save without name | Validation error shown | Not executed | Not Executed | Login blocked |

| SL-TC-08 | Create category with duplicate name | Category exists | Add category with same name | Duplicate error shown | Not executed | Not Executed | Login blocked |

| SL-TC-09 | Edit category name | Category exists | Edit category and save | Category updated | Not executed | Not Executed | Login blocked |

| SL-TC-10 | Delete category | Category exists | Delete category | Category removed or blocked | Not executed | Not Executed | Login blocked |

---

## Product Module

| SL-TC-11 | Create product with valid data | Category exists | Enter name, price, category → Save | Product created | Not executed | Not Executed | Login blocked |

| SL-TC-12 | Create product with empty name | Logged in | Leave name empty → Save | Validation error | Not executed | Not Executed | Login blocked |

| SL-TC-13 | Create product with invalid price | Logged in | Enter alphabetic price → Save | Validation error | Not executed | Not Executed | Login blocked |

| SL-TC-14 | Edit product details | Product exists | Edit product and save | Changes saved | Not executed | Not Executed | Login blocked |

| SL-TC-15 | Delete product | Product exists | Delete product | Product removed | Not executed | Not Executed | Login blocked |
