# Bug Report: Login Functionality Issue

## Bug ID: BUG-001
**Date Reported:** 2026-01-22  
**Reported By:** QA Team  
**Status:** Open  
**Priority:** High  
**Severity:** Major

---

## Summary
User cannot log in after entering valid credentials due to session timeout error.

---

## Description
When a user attempts to log in with valid credentials, the application displays a "Session timeout" error message even though no previous session existed. This prevents legitimate users from accessing their accounts.

---

## Steps to Reproduce
1. Navigate to Shelf Link login page (https://shelf-link.example.com/login)
2. Enter valid username: `testuser@example.com`
3. Enter valid password: `ValidPassword123!`
4. Click "Login" button
5. Observe the error message

---

## Expected Behavior
- User should be successfully authenticated
- User should be redirected to the dashboard
- Welcome message should be displayed

---

## Actual Behavior
- Error message appears: "Session timeout. Please try again."
- User remains on the login page
- Login attempt fails despite valid credentials

---

## Environment
- **Application Version:** 1.2.3
- **Browser:** Chrome 120.0.6099.109
- **Operating System:** Windows 11
- **Test Environment:** Staging

---

## Additional Information
- Issue occurs intermittently (approximately 60% of login attempts)
- Problem persists across different browsers (Chrome, Firefox, Safari)
- Clearing browser cache and cookies does not resolve the issue
- Issue does not occur in development environment

---

## Screenshots/Logs
```
[2026-01-22 08:30:15] ERROR: Session validation failed
[2026-01-22 08:30:15] INFO: User login attempt for testuser@example.com
[2026-01-22 08:30:15] ERROR: SessionNotFoundException: No active session found
```

---

## Suggested Fix
Investigate session management logic during the login process. The session check may be occurring before session creation, causing the false timeout error.

---

## Impact
- High impact on user experience
- Prevents legitimate users from accessing the application
- May result in increased support tickets
- Potential loss of user trust

---

## Related Issues
- Similar issue reported in BUG-045 (Password Reset Flow)
- May be related to recent session management updates in version 1.2.0
