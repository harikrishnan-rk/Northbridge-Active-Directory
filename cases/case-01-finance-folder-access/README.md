# Case 01 — Finance Folder Access Issue

## 🎫 Incident Summary

A Finance user reported that they could log in to `FIN-PC01` but could not access the Finance department shared folder.

**Ticket:** `NB-INC-001`
**Category:** File Access
**Priority:** Medium
**Role:** Helpdesk / Initial Triage

## 👤 My Responsibility

My responsibility was to:

* Confirm the affected user
* Reproduce the reported problem
* Perform basic client checks
* Collect initial evidence
* Escalate the issue to IT Support

No Active Directory, share, or NTFS permission changes were made during Helpdesk triage.

## 🔎 Initial Investigation

### 1. Confirm User Identity

The `whoami` command confirmed that the affected session was using the domain account:

`northbridge\sara.m`

**Evidence:**
[User-identity](evidence/helpdesk/01-user-identity.png)

### 2. Reproduce the Reported Issue

I attempted to access the Finance shared folder:

`\\SRV-DC01\Finance`

Windows returned an access-denied message indicating that the user did not have permission to access the resource.

**Evidence:**
[Finance-access-denied](evidence/helpdesk/02-finance-access-denied.png)

### 3. Confirm Client Information

The workstation was confirmed as:

`FIN-PC01`

The system information also showed the domain-qualified computer name:

`FIN-PC01.northbridge.local`

**Evidence:**
[Basic-client-check](evidence/helpdesk/03-basic-client-check.png)

## 📌 Helpdesk Finding

The affected user was able to log in successfully, but access to the Finance shared folder was denied.

At the Helpdesk stage, the specific cause of the authorization failure had not been established.

The issue was therefore escalated to IT Support for further investigation.

## 📸 Evidence

Helpdesk evidence is stored under:

[evidence/helpdesk/](evidence/helpdesk)

## 🔄 Escalation

**Escalation reason:**

The access failure was reproducible, but determining the cause required further investigation of the user's authorization and the Finance resource permissions.

## 💡 Lesson Learned

Successful Windows authentication does not automatically provide access to every network resource.

Helpdesk should first establish the user's identity, affected workstation, reported resource, and reproducible symptoms before escalating an access issue for administrative investigation.

## 🤝 Collaboration

This case was completed collaboratively by:

* [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk)
* [Mr. Manu P Nair](https://github.com/manunair16)
* [Mr. Varun M Nair](https://github.com/varunmnair95)

Each participant worked in an independent NorthBridge lab environment and maintained their own evidence and documentation.
