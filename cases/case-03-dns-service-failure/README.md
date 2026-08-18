# 🌐 Case 03 — DNS Service Failure

## 📌 Scenario

NorthBridge reported a DNS resolution problem affecting `MGT-PC01`.

The workstation could communicate with the domain controller, but DNS queries for `northbridge.local` were timing out.

The issue was investigated as a server-side DNS problem.

---

## 🎫 Incident Details

| Item              | Details                |
| ----------------- | ---------------------- |
| Ticket            | `NB-INC-003`           |
| Client            | `MGT-PC01`             |
| Domain Controller | `SRV-DC01`             |
| Domain            | `northbridge.local`    |
| DNS Server        | `SRV-DC01`             |
| DNS Server IP     | `192.168.29.10`        |
| Issue             | DNS Resolution Failure |
| Status            | Resolved               |

---

## 👥 Participants

| Participant                                                 | Role             | Repository                                                                           |
| ----------------------------------------------------------- | ---------------- | ------------------------------------------------------------------------------------ |
| [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk) | 📝 Documentation | [Hari's Repository](https://github.com/harikrishnan-rk/Northbridge-Active-Directory) |
| [Mr. Manu P Nair](https://github.com/manunair16)            | 🧑‍💻 Helpdesk   | [Manu's Repository](https://github.com/manunair16/northbridge-active-directory)      |
| [Mr. Varun M Nair](https://github.com/varunmnair95)         | 🛠️ IT Support   | [Varun's Repository](https://github.com/varunmnair95/northbridge-active-directory)   |

---

## 📝 My Role — Documentation

My responsibility was to document the incident, organize the investigation findings, record the root cause and resolution, and reference the evidence collected by the other participants.

No new technical screenshots were required for my role.

---

## 🔎 Investigation Summary

The initial investigation from `MGT-PC01` showed that DNS queries were timing out.

Basic connectivity to `SRV-DC01` remained available, indicating that the issue was not a complete network connectivity failure.

The issue was escalated for server-side investigation.

The server-side investigation confirmed that the DNS Server service on `SRV-DC01` was stopped.

---

## 🧠 Root Cause

The **DNS Server service on `SRV-DC01` was stopped**, preventing the domain controller from responding to DNS queries for `northbridge.local`.

---

## 🛠️ Resolution

The DNS Server service was started on `SRV-DC01`.

The service was confirmed to be running after the corrective action.

---

## ✅ Validation

DNS resolution was tested again from `MGT-PC01`.

The `northbridge.local` lookup successfully returned the DNS server address after the DNS service was restored.

This confirmed that the original DNS resolution problem had been resolved.

---

## 🔗 Investigation & Evidence

The client-side investigation and validation were performed by:

🧑‍💻 **[Manu — Helpdesk](https://github.com/manunair16/northbridge-active-directory/tree/main/cases/case-03-dns-service-failure)**

The server-side investigation and resolution were performed by:

🛠️ **[Varun — IT Support](https://github.com/varunmnair95/northbridge-active-directory/tree/main/cases/case-03-dns-service-failure)**

The evidence is maintained in the respective participant repositories instead of being duplicated.

---

## 💡 Lessons Learned

* 🔎 DNS resolution should be tested separately from basic network connectivity.
* 🌐 A server can remain reachable while its DNS service is unavailable.
* 🛠️ Server-side service status should be checked when client DNS queries fail.
* 📋 Evidence from each troubleshooting stage helps establish the root cause.
* ✅ Validation should confirm that the original reported problem has been resolved.

---

## 🤝 Collaboration

This case was completed collaboratively by:

* [Mr. Hari Krishnan R K](https://github.com/harikrishnan-rk)
* [Mr. Manu P Nair](https://github.com/manunair16)
* [Mr. Varun M Nair](https://github.com/varunmnair95)

Each participant maintained their own implementation and evidence in an independent NorthBridge Active Directory lab.
