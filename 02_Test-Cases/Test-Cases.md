# Test Cases for Shelf Link

## Overview
This document contains detailed test cases for the Shelf Link application.

---

## TC-001: User Login with Valid Credentials

**Priority:** High  
**Test Scenario:** User Authentication  
**Prerequisites:** User account exists in the system

### Test Steps:
1. Navigate to Shelf Link login page
2. Enter valid username/email
3. Enter valid password
4. Click "Login" button

### Expected Result:
- User is successfully authenticated
- User is redirected to the dashboard/home page
- Welcome message is displayed

---

## TC-002: User Login with Invalid Credentials

**Priority:** High  
**Test Scenario:** User Authentication  
**Prerequisites:** None

### Test Steps:
1. Navigate to Shelf Link login page
2. Enter invalid username/email
3. Enter invalid password
4. Click "Login" button

### Expected Result:
- Login fails
- Error message is displayed: "Invalid username or password"
- User remains on login page

---

## TC-003: Add New Book to Shelf

**Priority:** High  
**Test Scenario:** Book Management  
**Prerequisites:** User is logged in

### Test Steps:
1. Navigate to "Add Book" section
2. Enter book title
3. Enter author name
4. Enter ISBN (optional)
5. Select shelf (e.g., "Want to Read")
6. Click "Add Book" button

### Expected Result:
- Book is successfully added to the selected shelf
- Success message is displayed
- Book appears in the shelf list

---

## TC-004: Search for Book in Collection

**Priority:** Medium  
**Test Scenario:** Book Management  
**Prerequisites:** User is logged in and has books in collection

### Test Steps:
1. Navigate to user's book collection
2. Enter book title in search field
3. Press Enter or click Search button

### Expected Result:
- Search results display matching books
- Books are filtered based on search criteria
- "No results" message shown if no matches

---

## TC-005: Update Reading Status

**Priority:** Medium  
**Test Scenario:** Book Status Tracking  
**Prerequisites:** User is logged in and has books in collection

### Test Steps:
1. Navigate to book details
2. Click on status dropdown
3. Select new status (e.g., "Currently Reading")
4. Click "Save" or "Update"

### Expected Result:
- Book status is updated
- Book moves to appropriate shelf
- Update confirmation message is displayed

---

## TC-006: Delete Book from Shelf

**Priority:** High  
**Test Scenario:** Book Management  
**Prerequisites:** User is logged in and has books in collection

### Test Steps:
1. Navigate to shelf containing the book
2. Select book to delete
3. Click "Delete" or "Remove" button
4. Confirm deletion in popup/dialog

### Expected Result:
- Confirmation dialog appears
- After confirmation, book is removed from shelf
- Success message is displayed
- Book no longer appears in the collection

---

## Notes
- All test cases should be executed in the test environment before production deployment
- Test data should be reset between test runs for consistency
