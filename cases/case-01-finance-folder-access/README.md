# Case 01 — Finance Folder Access Issue

## 📌 Overview

A Finance user reported that they could log in to `FIN-PC01` but could not access the Finance shared folder.

This case was investigated as a collaborative troubleshooting exercise between [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk), [Mr. Manu P Nair](https://github.com/manunair16), and [Mr. Varun M Nair](https://github.com/varunmnair95).

Each participant worked in an independent NorthBridge lab environment.

## 👤 My Role

**Helpdesk / Initial Triage**

My responsibility was to:

* Receive and understand the reported issue
* Reproduce the problem
* Perform basic client-side checks
* Collect initial evidence
* Escalate the issue with useful information

## 🎫 Reported Issue

The Finance user could successfully log into Windows but received an access-denied error when attempting to access the Finance shared folder.

## 🔎 Initial Investigation

I confirmed:

* Windows authentication was successful.
* The workstation was functioning normally.
* The Finance folder access problem could be reproduced.
* The issue was related to access to the Finance resource rather than Windows login.

The issue was escalated to IT Support for further authorization and permission investigation.

## 📸 Evidence

Evidence for my Helpdesk investigation is stored under:

`evidence/helpdesk/`

## ✅ Outcome

IT Support identified and corrected the authorization issue. Finance folder access was subsequently validated successfully.

## 🤝 Collaboration

* [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk)
* [Mr. Manu P Nair](https://github.com/manunair16)
* [Mr. Varun M Nair](https://github.com/varunmnair95)

Each participant maintained their own screenshots, findings, and documentation.

## 💡 Lesson Learned

Helpdesk should establish the actual symptoms and gather useful information before making administrative changes. A successful Windows login does not necessarily mean the user is authorized to access every network resource.
