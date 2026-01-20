# Fields and Formula Fields

This section documents the important fields and formula fields used in the
Smart Service & Sales Management System (SSSMS).

---

## Formula Fields

### 1. Technician Assignment – Total Cost

**Object:** Technician_Assignment__c  
**Field Type:** Formula (Currency)

**Formula:**
Hours_Worked__c * Hourly_Rate__c


![Technician Assignment Forumala fileds](../Screenshots/Screenshot%202026-01-20%20081952.png)


**Purpose:**  
Automatically calculates the cost of technician work.

---

### 2. Service Request – Is High Priority?

**Object:** Service_Request__c  
**Field Type:** Formula (Checkbox)

**Formula:**
IF(Priority__c = 'High', TRUE, FALSE)


**Purpose:**  
Identifies high priority service requests for reporting and automation.
![Technician Assignment Forumala fileds](../Screenshots/Screenshot%202026-01-20%20082145.png)

---

### 3. Service Request – Service Duration (Days)

**Object:** Service_Request__c  
**Field Type:** Formula (Number)

**Formula:**
Closed_Date__c - CreatedDate

**Purpose:**  
Calculates the total number of days taken to complete a service request.
![Technician Assignment Forumala fileds](../Screenshots/Screenshot%202026-01-20%20082113.png)

---

## Key Non-Formula Fields

### Service_Request__c
- Service Cost (Currency)
- Status (Picklist)
- Priority (Picklist)
- Closed Date (Date)
- Technician (Lookup User)

### Technician_Assignment__c
- Hours Worked (Number)
- Hourly Rate (Currency)




