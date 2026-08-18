# 🔐 Case 02 — Account Lockout

## 📌 Scenario

Kevin Thomas, an Operations Executive, reported that he could not sign in to `OPS-PC01` because his NorthBridge domain account was locked.

The issue was intentionally simulated in the isolated NorthBridge Active Directory lab.

---

## 🎫 Incident Details

| Item              | Details             |
| ----------------- | ------------------- |
| Ticket            | `NB-INC-002`        |
| User              | Kevin Thomas        |
| Department        | Operations          |
| Client            | `OPS-PC01`          |
| Domain Controller | `SRV-DC01`          |
| Domain            | `northbridge.local` |
| Issue             | Account Lockout     |
| Status            | Resolved            |

---

## 👥 Participants

| Participant                                                 | Role             | Repository                                                                           |
| ----------------------------------------------------------- | ---------------- | ------------------------------------------------------------------------------------ |
| [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk) | 🛠️ IT Support   | [Hari's Repository](https://github.com/harikrishnan-rk/Northbridge-Active-Directory) |
| [Mr. Manu P Nair](https://github.com/manunair16)            | 📝 Documentation | [Manu's Repository](https://github.com/manunair16/northbridge-active-directory)      |
| [Mr. Varun M Nair](https://github.com/varunmnair95)         | 🧑‍💻 Helpdesk   | [Varun's Repository](https://github.com/varunmnair95/northbridge-active-directory)   |

---

## 🛠️ My Role — IT Support

My responsibility was to investigate the Active Directory account lockout, identify the source and root cause using Windows security evidence, perform remediation, and confirm the account was restored.

---

## 🔎 Investigation

### 1. Confirmed the account lockout

Kevin's account was checked in Active Directory Users and Computers.

📸 Evidence:

[Account-lockout](evidence/investigation/01-account-lockout.png)

### 2. Investigated Event ID 4740

The Security log on `SRV-DC01` was reviewed for Event ID `4740`.

The event was used to identify the account lockout and investigate the source of the lockout.

📸 Evidence:

[Event-4740](evidence/investigation/02-event-4740.png)

### 3. Root Cause

The root cause was determined by correlating the Active Directory account state with the relevant Security event evidence.

> **Multiple login attempt failure by the user above the account login threshold.**

---

## 🛠️ Resolution

After the source of the lockout was addressed, Kevin's account was unlocked.

The account was then checked to confirm that the lockout condition had been cleared.

---

## 🔗 Helpdesk Evidence

The initial triage was performed by:

🧑‍💻 **[Varun — Helpdesk](https://github.com/varunmnair95/northbridge-active-directory/tree/main/cases/case-02-account-lockout)**

---

## 🔗 Documentation & Validation

Final case documentation and validation were completed by:

📝 **[Manu — Documentation](https://github.com/manunair16/northbridge-active-directory)**

---

## 💡 Lessons Learned

* 🔎 Event ID 4740 provides valuable evidence when investigating AD account lockouts.
* 🧠 The account being locked is the symptom; the investigation must determine why it happened.
* 🛠️ The source of the failed authentication should be addressed before restoring access.
* ✅ Successful authentication should be used to validate the resolution.

---

## 🤝 Collaboration

This case was completed collaboratively by:

* [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk)
* [Mr. Manu P Nair](https://github.com/manunair16)
* [Mr. Varun M Nair](https://github.com/varunmnair95)

Each participant maintained their own implementation and evidence in an independent NorthBridge Active Directory lab.

