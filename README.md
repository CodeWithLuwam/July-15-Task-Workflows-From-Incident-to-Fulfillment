# ServiceNow Task Workflow: From Request to Fulfillment

This guide explains how a ServiceNow request flows from **Request** to **Requested Item** and finally to **Fulfillment Task**. Understanding this workflow is essential for managing approvals, assignments, and tracking in IT Service Management.

---

## 📚 Table of Contents
- [Overview](#overview)
- [Workflow Diagram](#workflow-diagram)
- [Navigation Path](#navigation-path)
- [Step 1: Access Your Request](#step-1-access-your-request)
- [Step 2: Review Requested Items](#step-2-review-requested-items)
- [Step 3: Open a Specific Requested Item](#step-3-open-a-specific-requested-item)
- [Step 4: Access Fulfillment Tasks](#step-4-access-fulfillment-tasks)
- [Step 5: Schema Map Overview](#step-5-schema-map-overview)
- [Summary](#summary)
- [Real-World Example](#real-world-example)

---

## Overview
In ServiceNow, a typical request workflow moves through **three layers**:

sc_request → sc_req_item → sc_task


- **Request (`sc_request`)**: Represents the entire order.
- **Requested Item (`sc_req_item`)**: Represents individual items in the order.
- **Task (`sc_task`)**: Represents actions required to fulfill each item.

---

## ✅ Step 1: Access Your Request
1. Navigate to **All > Self Service > My Requests**.
2. Click the **Request Number** (e.g., `REQ0000001`) to open the request details.

![](https://github.com/CodeWithLuwam/July-15-Task-Workflows-From-Incident-to-Fulfillment/blob/main/Images/Request%20Record.png?raw=true)  
**Figure 1:** Request record showing request details.

---

## ✅ Step 2: Review Requested Items
- Scroll to the **Requested Items** tab.
- Here you’ll find all items in the order, such as:
  - Standard Laptop
  - Samsung Galaxy S7
  - iPad 3

> **Tip:** Each item can have different processing stages. For example:
> - A laptop may go through **Security approval** before shipping.
> - A phone may ship directly to the requester.

![](https://github.com/CodeWithLuwam/July-15-Task-Workflows-From-Incident-to-Fulfillment/blob/main/Images/Request%20Items%20tab%20Different%20Processing%20Stages.png?raw=true)  
**Figure 2:** Requested Items tab listing all items in the order.

---

## ✅ Step 3: Open a Specific Requested Item
1. Click on a **Requested Item number** (e.g., `RITM0000002`).
2. You’ll see:
   - **Catalog Tasks(1)**
      - Shows a related task (**TASK0000001**)
   - **Approvers** tab (currently empty)
   - **Group approvals** tab (currently empty)

![](https://github.com/CodeWithLuwam/July-15-Task-Workflows-From-Incident-to-Fulfillment/blob/main/Images/Request%20Item.png?raw=true)  
**Figure 3:** Requested Item record details.

---

## ✅ Step 4: Access Fulfillment Tasks
1. From the Requested Item record, click the **Task number** under the **Tasks** related list.
2. Inside the Task record, you’ll find:
   - **Assigned To**: Person or team fulfilling the task
   - **Status & Priority**
   - **Approval workflow**
   - **Affected CIs** (Configuration Items)

> **Note:** One Requested Item can have multiple tasks handled by different departments:
> - Shipping → Security Check → Software Installation → Delivery.

![](https://github.com/CodeWithLuwam/July-15-Task-Workflows-From-Incident-to-Fulfillment/blob/main/Images/From%20the%20Requested%20Item%20Record,%20Click%20the%20Task%20Number.png?raw=true)  
**Figure 4:** Task record with assignment and status details.

---

## ✅ Step 5: Schema Map Overview
1. Navigate to: **All > System Definition > Tables**.
2. Open the **Request table** and click **Schema Map**:
   - Shows relationships between **Task**, **Request**, and **Requested Item**.
3. Open the **Task table** schema map:
   - Confirms the hierarchy:  

  ![](https://github.com/CodeWithLuwam/July-15-Task-Workflows-From-Incident-to-Fulfillment/blob/main/Images/Schema%20Map%20Overview.png?raw=true)   

---

## ✅ Summary
- **Request (sc_request)**: Entire order.
- **Requested Item (sc_req_item)**: Individual items.
- **Task (sc_task)**: Fulfillment steps.

---

## ✅ Real-World Example
- Order a Laptop → Security Approves → IT Installs Software → Ship to Employee.


