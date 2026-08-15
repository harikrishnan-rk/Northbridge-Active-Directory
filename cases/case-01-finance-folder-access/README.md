# 🔐 Case 01 — Finance Folder Access Issue

## 📌 Case Summary

A Finance user reports that they are unable to access the Finance department shared folder from the `FIN-PC01` workstation.

The objective is to investigate the reported access problem, identify the root cause, restore appropriate access, and validate the resolution.

This case is a collaborative exercise between [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk), [Mr. Manu P Nair](https://github.com/manunair16), and [Mr. Varun M Nair](https://github.com/varunmnair95), with each participant working in an independent lab environment and maintaining their own evidence and documentation.

---

## 🖥️ Environment

| Component                | Details                          |
| ------------------------ | -------------------------------- |
| 🌐 Domain                | `northbridge.local`              |
| 🖥️ Domain Controller    | `SRV-DC01`                       |
| 💻 Finance Workstation   | `FIN-PC01`                       |
| 📂 Resource              | Finance department shared folder |
| 👥 Expected Access Group | `GG_Finance`                     |

---

## 🤝 Case Roles

| Participant                                                 | Role                        | Primary Responsibility                                                 |
| ----------------------------------------------------------- | --------------------------- | ---------------------------------------------------------------------- |
| [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk) | 🧑‍💻 Initial Triage        | User report, reproduction, initial checks and evidence collection      |
| [Mr. Manu P Nair](https://github.com/manunair16)            | 🔍 Technical Investigation  | AD groups, share permissions, NTFS permissions and root-cause analysis |
| [Mr. Varun M Nair](https://github.com/varunmnair95)         | 🛠️ Resolution & Validation | Remediation, access testing and final validation                       |

### My Role

**Initial Triage**

My responsibility is to perform the first-level investigation of the reported Finance folder access problem.

I will focus on:

* 📋 Reviewing the reported issue
* 💻 Reproducing the problem from `FIN-PC01`
* 👤 Verifying the affected user
* 👥 Checking relevant group membership
* 🌐 Performing basic connectivity checks
* 📸 Collecting initial evidence
* 📝 Documenting initial findings
* 🔄 Handing off the findings for deeper technical investigation

---

## 🔎 Investigation Flow

```text
User Report
    ↓
Initial Access Test
    ↓
User Verification
    ↓
Group Membership Check
    ↓
Basic Connectivity Check
    ↓
Evidence Collection
    ↓
Technical Investigation
    ↓
Remediation
    ↓
Validation
    ↓
Case Closure
```

---

## 📸 Evidence

Evidence collected during the initial triage will be stored under:

`evidence/`

The evidence will focus on the reported user impact and observations **before remediation**.

---

## 📊 Case Status

**Status:** 🔄 Initial Triage

**Root Cause:** To be determined

**Resolution:** To be determined

**Validation:** Pending

---

## 🔗 Collaboration

This case demonstrates a collaborative troubleshooting workflow while maintaining individual ownership of each participant's work.

Each participant maintains:

* 🧪 An independent lab environment
* 📸 Their own screenshots and evidence
* 📝 Their own findings and documentation
* 👤 Their assigned role within the case

The repositories are maintained independently rather than combining all three participants' work into a single repository.
