# Validation Rules

This project uses validation rules to maintain data quality and enforce critical business logic.

---

## 1. Close Service Request Only When Service Cost Exists

**Object:** Service_Request__c

**Description:**  
Prevents users from closing a service request unless the service cost is entered.

**Formula:**
AND(
ISPICKVAL(Status__c, 'Completed'),
ISBLANK(Service_Cost__c)
)


**Error Message:**  
Service Cost must be entered before closing the request.

---

## 2. High Priority Service Must Have Technician Assigned

**Object:** Service_Request__c

**Description:**  
Ensures that all high priority service requests have an assigned technician.

**Formula:**
AND(
ISPICKVAL(Priority__c, 'High'),
ISBLANK(Technician__c)
)

**Error Message:**  
Technician must be assigned for High Priority service requests.

