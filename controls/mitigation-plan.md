# Mitigation Plan

## Control portfolio

| ID | Control | LINDDUN strategy | Owner | Evidence | Priority |
| --- | --- | --- | --- | --- | --- |
| C01 | Collect and expose only the attributes required for each workflow | Minimize | Product owner and data owner | Approved field inventory and API response tests | Critical |
| C02 | Replace shared student identifiers with purpose-scoped pseudonymous identifiers | Separate and minimize | Solution architect | Identifier design and cross-context linkage test | High |
| C03 | Enforce role and field level authorization for instructors, registry staff, and administrators | Control and enforce | IAM owner | Access matrix, policy configuration, and denial tests | Critical |
| C04 | Encrypt backups with university controlled keys and isolate backup administration | Hide and separate | Infrastructure owner | Key configuration, access review, and restore test | Critical |
| C05 | Apply minimum cohort thresholds, suppression, and review to statistical outputs | Aggregate and minimize | Analytics owner | Disclosure-control rules and small-group tests | High |
| C06 | Replace unmanaged Bluetooth transfer with an authenticated, encrypted, expiring download | Hide and control | Product owner | Export design and expiry tests | High |
| C07 | Define purpose-based retention for records, logs, SMS metadata, and backups | Minimize and enforce | Data owner and DPO | Retention schedule and deletion evidence | High |
| C08 | Govern cloud and SMS providers through due diligence, contract terms, subprocessor review, and deletion assurance | Enforce and demonstrate | Procurement and DPO | Processor register, agreements, and review records | High |
| C09 | Provide layered and just-in-time notices for cloud, SMS, analytics, and delegated processing | Inform | Privacy lead and UX owner | Notice copy, interface evidence, and comprehension test | High |
| C10 | Review privileged access, log sensitive actions, and show users an appropriate activity history | Control and demonstrate | Security operations | Quarterly review evidence and audit samples | High |
| C11 | Protect exports and notifications from unnecessary content and metadata | Hide and minimize | Engineering owner | Message templates, export configuration, and leak tests | Medium |
| C12 | Maintain privacy assurance evidence and formally accept residual risk | Demonstrate | System owner and DPO | Signed review, test results, and residual risk record | High |

## Delivery sequence

### Phase 1: Reduce concentrated exposure

Implement C01, C03, and C04 first. They address the critical database scenario and the largest disclosure path.

### Phase 2: Restrict secondary use

Implement C02, C05, C06, and C07. These controls reduce linkage, statistical re-identification, unmanaged export, and unnecessary retention.

### Phase 3: Make processing understandable and auditable

Implement C08 through C12. This phase produces provider assurance, user-facing transparency, access evidence, and formal residual-risk decisions.

## Residual risk decision

The system owner should not accept residual risk until the verification plan demonstrates that high and critical scenarios have effective controls. Legal obligations remain mandatory regardless of the numerical score.
