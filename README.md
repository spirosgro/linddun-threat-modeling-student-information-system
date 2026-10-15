# Privacy Threat Modeling with LINDDUN

An end-to-end privacy threat model for a university student information subsystem. The project converts a data-flow model into traceable LINDDUN threats, risk decisions, privacy requirements, mitigations, and verification evidence.

![Student information system privacy threat model](docs/linddun-threat-model-cover.png)

## What this project demonstrates

- Data-flow modeling across user, application, database, cloud, mobile, and analytics boundaries
- Systematic use of all seven LINDDUN threat categories
- A reproducible 5 x 5 privacy risk method with explicit assumptions
- Traceability from each threat scenario to a privacy requirement, control, owner, and verification step
- Clear separation between the original academic scope and the portfolio extension

## Executive finding

The most serious risks arise where stable student identifiers and academic records accumulate in the central database and cloud backup. The model also identifies material transparency gaps around cloud storage, SMS processing, administrative access, and secondary analytics. The recommended design reduces linkability and identifiability through scoped identifiers, aggregation, and pseudonymization; restricts disclosures through encryption and role design; and turns transparency obligations into testable product requirements.

## Case study scope

The modeled system supports student profile management, academic records, course administration, statistical requests, cloud backups, SMS verification, and optional transfer of documents from a personal computer to a smartphone. The assessment is based on a university assignment scenario and does not describe a production environment.

The original team assignment examined **Identifiability** and **Unawareness**. This public portfolio edition preserves those eight scenarios and adds a clearly labeled extension across Linkability, Non-repudiation, Detectability, Data Disclosure, and Non-compliance.

## Repository map

| Path | Purpose |
| --- | --- |
| [`report/privacy-threat-modeling-linddun.docx`](report/privacy-threat-modeling-linddun.docx) | Complete English report |
| [`presentation/privacy-threat-modeling-linddun.pptx`](presentation/privacy-threat-modeling-linddun.pptx) | Executive presentation |
| [`model/system-model.md`](model/system-model.md) | Scope, assets, actors, trust boundaries, and assumptions |
| [`model/data-flow-inventory.csv`](model/data-flow-inventory.csv) | Structured DFD inventory |
| [`analysis/linddun-threat-register.csv`](analysis/linddun-threat-register.csv) | Threat, score, requirement, and control traceability |
| [`analysis/risk-method.md`](analysis/risk-method.md) | Scoring method and interpretation rules |
| [`controls/mitigation-plan.md`](controls/mitigation-plan.md) | Prioritized privacy controls and ownership |
| [`controls/verification-plan.md`](controls/verification-plan.md) | Testable acceptance criteria |
| [`docs/project-provenance.md`](docs/project-provenance.md) | Academic origin, public edition, and authorship boundary |
| [`references/references.md`](references/references.md) | Primary and authoritative sources |

## Method

1. Define the system, personal data, actors, and trust boundaries.
2. Map entities, processes, stores, and flows.
3. Apply the seven LINDDUN categories to relevant DFD elements.
4. Write concrete threat scenarios with a clear affected data subject.
5. Score likelihood and impact on a 1–5 scale.
6. Convert material threats into privacy requirements and controls.
7. Define verification evidence before accepting residual risk.

## Priority risks

| ID | Scenario | Score | Priority |
| --- | --- | ---: | --- |
| I-01 | Re-identification through combined student records | 20 | Critical |
| U-01 | Students are not clearly informed about cloud backups | 16 | High |
| DD-02 | A cloud backup incident exposes complete student records | 15 | High |
| NC-02 | Third-party processing lacks complete contractual and transfer evidence | 15 | High |
| L-01 | A stable identifier links activity across system contexts | 16 | High |

## Recommended control sequence

1. Replace broadly reused identifiers with purpose-scoped identifiers.
2. Encrypt and isolate backups, enforce least privilege, and test restoration separately from production access.
3. Apply aggregation thresholds and disclosure controls to statistical requests.
4. Provide layered, just-in-time notices for cloud, SMS, and delegated administrative processing.
5. Establish retention, processor assurance, access review, and privacy test evidence.

## Limitations

This is a design-level assessment based on a supplied scenario. It does not include source-code review, production configuration, interviews, DPIA approval, penetration testing, or legal advice. Scores represent reasoned assumptions and should be recalibrated with system owners and data protection specialists before operational use.

## Responsible publication

The public edition removes student registration numbers, university branding, and personal contact details. It identifies the work as a team assignment without publishing the other students' names pending their consent. See [`docs/project-provenance.md`](docs/project-provenance.md).

## Author

Public portfolio edition prepared by **Spyridon Grouztidis** from a four-person academic team project.

## License

No reuse license is granted for the academic content. See [`LICENSE.md`](LICENSE.md).
