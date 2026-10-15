# Verification Plan

| Test ID | Control | Verification procedure | Acceptance criterion | Evidence owner |
| --- | --- | --- | --- | --- |
| V01 | C01 | Compare every API and screen field with the approved purpose inventory | No unapproved attribute appears in a response, export, or administrative view | Product owner |
| V02 | C02 | Attempt to correlate identifiers across portal, analytics, logs, and backup indexes | Cross-context linkage requires an approved, separately controlled mapping | Solution architect |
| V03 | C03 | Run positive and negative authorization tests for each role and sensitive field | Every unauthorized request is denied and logged | IAM owner |
| V04 | C04 | Review encryption, key custody, backup administrator access, and restoration | Backup content remains unreadable without university-controlled key access | Infrastructure owner |
| V05 | C05 | Query statistics for small and intersecting cohorts | Results below the approved threshold are suppressed or generalized | Analytics owner |
| V06 | C06 | Inspect exported files, links, devices, and expiry behavior | Export uses an authenticated encrypted channel and expires as designed | Engineering owner |
| V07 | C07 | Seed records at each retention boundary and run deletion jobs | Data, logs, provider metadata, and backups expire according to the approved schedule | Data owner |
| V08 | C08 | Review provider agreements, subprocessors, transfer basis, deletion, and incident terms | Required documents are current, approved, and linked to the processor register | Procurement and DPO |
| V09 | C09 | Test notices at cloud backup, SMS verification, analytics, and delegated-processing touchpoints | Users can identify purpose, recipient, retention, and rights without leaving the task flow | Privacy lead |
| V10 | C10 | Sample privileged access and compare it with approved roles and tickets | All sampled access is authorized, attributable, and reviewed within the target period | Security operations |
| V11 | C11 | Inspect notification bodies and exported metadata | No unnecessary academic, identity, or diagnostic data leaves the system | Engineering owner |
| V12 | C12 | Trace each high or critical threat to implemented controls and test evidence | Every material threat has an owner, passing evidence, residual score, and decision | System owner and DPO |

## Reassessment triggers

Repeat the threat model when the system introduces a new identity provider, analytics use, mobile application, cloud region, processor, dataset, or cross-system integration. Reassess after a privacy incident or a material change to retention or access policy.
