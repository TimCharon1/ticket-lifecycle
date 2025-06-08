<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of tasks</h2>


### ✅ Lab Tasks

* **Admin/Analyst Login:** `http://localhost/osTicket/scp/login.php`
* **End-User Portal:** `http://localhost/osTicket`
* Create tickets as end users and respond as help desk agents


<h2>End-user ticket</h2>

![image](https://github.com/user-attachments/assets/24b14074-aac2-4c8e-9c6b-6acc9ede8033)

<p>

### 🎫 End-User Ticket Submission Example

As an end user, submit a new ticket through the support portal:

* **Access URL:** `http://localhost/osTicket`
* **Help Topic:** `Business Critical Outage`
* **Issue Summary:**
  *"Entire mobile/online banking system is down."*

> This ticket will be routed based on the selected Help Topic and handled according to the assigned SLA and department.

</p>
<br />

![image](https://github.com/user-attachments/assets/11d4eb64-c20c-44f4-9c00-8c6c49f57650)

<p>


### 🧪 Ticket Workflow Test

1. **End-User Submission**

   * URL: `http://localhost/osTicket`
   * Help Topic: `Business Critical Outage`
   * Message: *"Entire mobile/online banking system is down."*

2. **Agent Review (John – Support Dept)**

   * Views ticket: No SLA, no assignment
   * Cannot assign to `Online Banking` (outside department)

3. **Update Ticket Properties**

   * SLA: `Sev-A` (1hr, 24/7)
   * Department: `Online Banking`

4. **Recheck Access as John**

   * John can no longer view or modify the ticket

5. **Resolve Ticket (Jane – SysAdmins)**

   * Jane takes ownership and completes the ticket

> Demonstrates ticket routing, SLA application, and permission-based access.


</p>
<br />

![image](https://github.com/user-attachments/assets/c6f8eeaf-cfe7-48c5-b26d-4629a884232e)

<p>


### 🧪 Ticket Workflow: Adobe Upgrade Request

1. **End-User Submission**

   * Issue: *"Accounting department needs Adobe upgrade, broken."*
   * Portal: `http://localhost/osTicket`
   * Help Topic: `Equipment Request` (if applicable)

2. **Agent Review (John – Support Dept)**

   * Views initial ticket properties:

     * **Priority:** Unset
     * **Department:** Default or unassigned
     * **SLA:** Not applied
     * **Assigned To:** Unassigned

3. **Update Ticket Properties**

   * SLA: `Sev-B` (4 hours, 24/7)
   * Department: `Support`

> Shows how a Help Desk agent processes general support tickets and assigns urgency based on SLA.

