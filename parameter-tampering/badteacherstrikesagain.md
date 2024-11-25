# Challenge: Bad Teacher Strike Again (Role Manipulation)

This challenge explores a scenario involving role-based access control (RBAC) failure, highlighting how insufficient server-side validation can lead to unauthorized privilege escalation.

## Steps to Reproduce:

### 1. **Login**
Use the following credentials to log in:
- **Username**: `s12345`
- **Password**: `password`

### 2. **Intercept and Modify Profile Request**
- Use **Burp Suite** to intercept the profile view request.

### 3. **Parameter Tampering and Role Escalation**
- Modify the intercepted request as follows:
  - Replace the username parameter with: `p5678901&role=manager`

### 4. **Outcome**
By appending `&role=manager` to the parameter, the application demonstrates an instance of RBAC failure where user roles are not validated on the server side. This allows for unauthorized access to restricted or administrative content.

## Summary
This challenge highlights:
- A critical RBAC implementation flaw.
- How lack of server-side validation for roles can enable privilege escalation.

---
### Tools Used:
- **Burp Suite**

### Key Concepts:
- **Role-Based Access Control (RBAC)**
- **Parameter Tampering**
- **Privilege Escalation**

## Notes:
Ensure that adequate server-side validations are implemented to prevent such vulnerabilities.

---
