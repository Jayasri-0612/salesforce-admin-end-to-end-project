# Security Model

This section explains how data security is implemented in the Smart Service & Sales Management System (SSSMS)
to ensure users only access data relevant to their roles.

---

## Org-Wide Defaults (OWD)

| Object | Access Level |
|------|-------------|
| Account | Private |
| Service_Request__c | Private |
| Technician_Assignment__c | Controlled by Parent |

---

## Profiles

### Admin Profile
- Full access to all objects and records
- Manage users, security, and automation

### Service Agent Profile
- Read and Create Service Requests
- Edit own Service Requests
- No delete access

### Technician Profile
- Read-only access to Accounts
- Edit access to Technician Assignments
- Limited access to Service Requests

---

## Permission Sets

### Additional Service Cost Access
- Provides extra edit access to Service Cost field
- Assigned without changing user profile

---

## Security Benefits
- Ensures data confidentiality
- Prevents unauthorized record access
- Supports role-based access control
