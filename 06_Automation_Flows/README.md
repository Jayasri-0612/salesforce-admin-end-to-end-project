# Automation using Salesforce Flows

This project uses Salesforce Flows to automate service management processes
and reduce manual effort.

---

## 1. Record-Triggered Flow

**Object:** Service_Request__c  
**Trigger Condition:** Status = Completed  

### Actions Performed
1. Automatically set Closed Date
2. Send email notification to Account Owner
3. Create Payment__c record

**Business Benefit:**  
Ensures consistent service closure and automatic payment tracking.

---

## 2. Screen Flow – Create Service Request

**Use Case:** Guided service request creation

### Screens
1. Select Account
2. Enter Priority and Description
3. Assign Technician
4. Confirmation Screen

**Business Benefit:**  
Improves user experience and reduces data entry errors.

---

## 3. Scheduled Flow

**Schedule:** Daily at midnight

### Logic
- Identify Service Requests with status "In Progress" for more than 7 days
- Automatically update Priority to High

**Business Benefit:**  
Prevents service delays and ensures timely resolution of requests.
