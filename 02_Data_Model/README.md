# Data Model

This section describes the data model used in the Smart Service & Sales Management System (SSSMS).

---

## Standard Objects Used

### Account (Customer)
Represents customers who purchase products and request after-sales services.

### Contact (Customer Contact)
Represents individual contacts associated with customer accounts.

### Opportunity (Sales Order)
Represents product sales orders.

### User
Represents internal users such as Admins, Service Agents, and Technicians.

---

## Custom Objects

### Service_Request__c
Represents customer service tickets.

**Fields**
- Service Request Number (Auto Number)
- Account (Lookup Account)
- Contact (Lookup Contact)
- Status (Picklist: New, In Progress, Completed, Cancelled)
- Priority (Picklist: Low, Medium, High)
- Service Cost (Currency)
- Technician (Lookup User)
- Closed Date (Date)

---

### Technician_Assignment__c
Tracks technician work performed for a service request.

**Fields**
- Assignment Name (Auto Number)
- Service Request (Master-Detail Service_Request__c)
- Technician (Lookup User)
- Hours Worked (Number)
- Hourly Rate (Currency)
- Total Cost (Formula)

---

### Payment__c
Tracks payments for completed services.

**Fields**
- Payment Number (Auto Number)
- Service Request (Lookup Service_Request__c)
- Amount Paid (Currency)
- Payment Status (Picklist: Pending, Paid)

---

## Object Relationships

| Parent | Child | Relationship |
|------|------|-------------|
| Account | Service_Request__c | Lookup |
| Service_Request__c | Technician_Assignment__c | Master-Detail |
| Service_Request__c | Payment__c | Lookup |

---



## Service_Request__c Object

Represents customer service tickets.

![Service Request Object](../Screenshots/Screenshot%202026-01-19%20085746.png)

---

## Service_Request Custom Object and their fields.

![Service Request Object](../Screenshots/Screenshot%202026-01-19%20085857.png)
---

## Technician Assignment Custom Object and their fields.

![Service Request Object](../Screenshots/Screenshot%202026-01-19%20085951.png)

---

## Payment Object and their fields.

![Service Request Object](../Screenshots/Screenshot%202026-01-19%20090030.png)

---

## Relationship Between Objects.

![Service Request Object](../Screenshots/Screenshot%202026-01-19%20091137.png)



