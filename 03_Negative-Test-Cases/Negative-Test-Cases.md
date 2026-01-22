# Negative Test Cases for Shelf Link

## Overview
This document contains negative test cases to verify that the Shelf Link application handles invalid inputs and error conditions correctly.

---

## NTC-001: Login with Empty Username

**Priority:** High  
**Test Scenario:** User Authentication - Negative

### Test Steps:
1. Navigate to login page
2. Leave username field empty
3. Enter valid password
4. Click "Login" button

### Expected Result:
- Login fails
- Error message displayed: "Username is required"
- Login button may be disabled until field is filled

---

## NTC-002: Login with Empty Password

**Priority:** High  
**Test Scenario:** User Authentication - Negative

### Test Steps:
1. Navigate to login page
2. Enter valid username
3. Leave password field empty
4. Click "Login" button

### Expected Result:
- Login fails
- Error message displayed: "Password is required"
- User remains on login page

---

## NTC-003: Add Book with Missing Required Fields

**Priority:** High  
**Test Scenario:** Book Management - Negative

### Test Steps:
1. Log in successfully
2. Navigate to "Add Book" page
3. Leave title field empty
4. Enter author name
5. Click "Add Book" button

### Expected Result:
- Book is not added
- Error message displayed: "Book title is required"
- Form validation prevents submission

---

## NTC-004: SQL Injection in Search Field

**Priority:** Critical  
**Test Scenario:** Security Testing

### Test Steps:
1. Log in successfully
2. Navigate to search functionality
3. Enter SQL injection payload: `' OR '1'='1`
4. Execute search

### Expected Result:
- Application properly sanitizes input
- No database error is displayed
- No unauthorized data is returned
- Search returns no results or handles safely

---

## NTC-005: XSS Attack in Book Title

**Priority:** Critical  
**Test Scenario:** Security Testing

### Test Steps:
1. Log in successfully
2. Navigate to "Add Book" page
3. Enter script tag in title: `<script>alert('XSS')</script>`
4. Fill other required fields
5. Submit form

### Expected Result:
- Input is properly escaped/sanitized
- Script does not execute
- Data is stored safely without executing malicious code

---

## NTC-006: Register with Existing Email

**Priority:** High  
**Test Scenario:** User Registration - Negative

### Test Steps:
1. Navigate to registration page
2. Enter email that already exists in system
3. Fill other required fields
4. Click "Register" button

### Expected Result:
- Registration fails
- Error message displayed: "Email already exists"
- User is not created
- Existing user data is not affected

---

## NTC-007: Upload Invalid File Type as Profile Picture

**Priority:** Medium  
**Test Scenario:** File Upload - Negative

### Test Steps:
1. Log in successfully
2. Navigate to profile settings
3. Click "Upload Profile Picture"
4. Select executable file (.exe) or other non-image file
5. Attempt to upload

### Expected Result:
- Upload fails
- Error message: "Invalid file type. Please upload an image"
- Profile picture is not changed
- No security vulnerability exploited

---

## NTC-008: Add Book with Extremely Long Title

**Priority:** Medium  
**Test Scenario:** Input Validation - Negative

### Test Steps:
1. Log in successfully
2. Navigate to "Add Book" page
3. Enter title with 1000+ characters
4. Fill other fields
5. Submit form

### Expected Result:
- Input validation limits character count
- Error message: "Title exceeds maximum length"
- Or title is truncated with warning
- Database constraints prevent overflow

---

## NTC-009: Access Protected Page Without Authentication

**Priority:** Critical  
**Test Scenario:** Authorization - Negative

### Test Steps:
1. Do not log in
2. Directly access URL of protected page (e.g., /dashboard, /my-books)
3. Observe behavior

### Expected Result:
- Access is denied
- User is redirected to login page
- Error message: "Please log in to access this page"
- Session management is enforced

---

## NTC-010: Delete Book Belonging to Another User

**Priority:** Critical  
**Test Scenario:** Authorization - Negative

### Test Steps:
1. Log in as User A
2. Obtain book ID belonging to User B
3. Attempt to delete book via direct URL manipulation or API call
4. Observe result

### Expected Result:
- Deletion fails
- Error message: "Unauthorized action"
- Book remains in User B's collection
- Proper authorization checks are enforced

---

## Notes
- These negative test cases are critical for security and data integrity
- All negative scenarios should fail gracefully with appropriate error messages
- Security-related tests should be prioritized and executed regularly
