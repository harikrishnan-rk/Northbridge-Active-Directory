# Helpdesk Ticket — NB-INC-001

## Ticket Information

| Field       | Details                   |
| ----------- | ------------------------- |
| Ticket      | `NB-INC-001`              |
| Category    | File Access               |
| Priority    | Medium                    |
| User        | `northbridge\sara.m`      |
| Workstation | `FIN-PC01`                |
| Resource    | `\\SRV-DC01\Finance`      |
| Role        | Helpdesk / Initial Triage |
| Status      | Escalated to IT Support   |

## User Report

The Finance user reported that they could successfully log in to the workstation but could not access the Finance shared folder.

## Initial Checks

The following checks were performed:

1. Confirmed the logged-in user account using `whoami`.
2. Confirmed the workstation as `FIN-PC01`.
3. Attempted to access the Finance shared folder.
4. Confirmed that the access failure could be reproduced.

## Findings

The user was successfully authenticated to the Windows workstation.

Access to:

`\\SRV-DC01\Finance`

was denied.

At this stage, the specific cause of the access failure was not determined.

## Evidence

* [User identity](../evidence/helpdesk/01-user-identity.png)
* [Finance access denied](../evidence/helpdesk/02-finance-access-denied.png)
* [Client information](../evidence/helpdesk/03-basic-client-check.png)

## Escalation

The issue was escalated to IT Support because further investigation of the user's authorization and the Finance resource permissions was required.

No Active Directory, share, or NTFS permission changes were made during Helpdesk triage.

## Helpdesk Conclusion

The reported access problem was confirmed and documented.

The case was handed over to IT Support for technical investigation and root-cause analysis.

