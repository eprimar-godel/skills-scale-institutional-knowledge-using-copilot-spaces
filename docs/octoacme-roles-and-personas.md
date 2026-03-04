# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises. For a quick view of role accountability per project phase and cross-role handoff checklists, see the [RACI & Handoffs guide](octoacme-raci-and-handoffs.md).

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

## QA / Testing

### Role Summary
QA/Testing engineers validate that delivered features meet acceptance criteria and quality standards before release. They design and execute test plans, automate regression suites, and act as the final quality gate.

### Responsibilities
- Design test plans and test cases aligned with acceptance criteria
- Automate regression and smoke-test suites
- Perform exploratory and usability testing
- Report defects with clear reproduction steps and severity ratings
- Verify fixes and sign off on release readiness

### Goals
- Prevent regressions and catch defects early in the lifecycle
- Increase automated test coverage sprint-over-sprint
- Provide clear, timely quality signals to the team

### Typical Communication
- Test results and bug reports in the issue tracker
- Go/no-go signal for releases in the release checklist
- Participation in sprint reviews and retrospectives

### How this role interacts with others
| Interacts With | Collaboration / Handoff |
|---|---|
| Developers | Receives completed features for QA; collaborates on reproduction steps and fix verification |
| PM | Reports quality status and blockers; escalates release-blocking defects |
| PdM | Validates acceptance criteria coverage; flags gaps in requirements |
| Security Lead | Coordinates on security test cases and vulnerability scan results |
| UX/UI Designer | Performs usability checks against design specs |
| Technical Writer | Reviews user-facing copy and error messages for accuracy |

---

## UX/UI Designer

### Role Summary
UX/UI Designers own user experience and interface quality across the product. They translate user needs and business requirements into intuitive designs, working closely with PdM and Developers throughout the product lifecycle.

### Responsibilities
- Conduct user research and usability testing to inform design decisions
- Create wireframes, prototypes, and high-fidelity design specs
- Define and maintain the design system and UI component library
- Review implemented UI against design specs and raise discrepancies
- Participate in backlog refinement to flag UX implications of upcoming work
- Deliver accessibility-compliant designs

### Goals
- Ensure the product is intuitive, accessible, and delightful for end users
- Reduce redesign churn by establishing clear design patterns early
- Continuously improve usability based on research and feedback

### Typical Communication
- Design reviews and prototype walkthroughs with PdM and Developers
- Usability test reports shared with PM and PdM
- Design files and component specs linked in relevant backlog items

### How this role interacts with others
| Interacts With | Collaboration / Handoff |
|---|---|
| PdM | Aligns on user problems and product vision before starting design work; participates in roadmap planning |
| Developers | Delivers finalized design specs and assets; reviews implementation for fidelity; unblocks technical questions about design intent |
| PM | Flags design-related risks and timeline impacts; reports on usability testing milestones |
| QA/Testing | Provides design specs as acceptance criteria reference; supports exploratory usability testing |
| Business Analyst | Incorporates business requirements and user research insights into design decisions |
| Stakeholder Representative | Gathers feedback from stakeholder groups on prototypes before development begins |

---

## Technical Writer

### Role Summary
Technical Writers create and maintain user documentation, API references, release notes, and internal knowledge-base articles. They ensure documentation is accurate, accessible, and aligned with the shipped product.

### Responsibilities
- Author and update user guides, onboarding docs, and help content
- Maintain API and SDK documentation in sync with code changes
- Draft and publish release notes for each release
- Collaborate with Developers and PdM to ensure technical accuracy
- Establish and enforce documentation standards and style guides
- Support knowledge-sharing efforts, including internal runbooks and wikis

### Goals
- Ensure users and support teams can self-serve effectively using documentation
- Reduce support ticket volume caused by unclear or missing documentation
- Keep documentation up-to-date with each release

### Typical Communication
- Review requests on PRs that include user-facing or API changes
- Release note drafts shared with PM and PdM for review before each release
- Documentation tickets tracked in the project backlog

### How this role interacts with others
| Interacts With | Collaboration / Handoff |
|---|---|
| Developers | Reviews code changes to understand documentation impact; requests technical reviews of drafted content |
| PdM | Aligns docs scope with feature priorities; receives feature specs for doc planning |
| PM | Coordinates documentation milestones with the release schedule; flags doc-related risks |
| QA/Testing | Requests review of procedural steps and error messages for accuracy |
| Security Lead | Documents security advisories, incident communications, and security-related procedures |
| Stakeholder Representative | Gathers feedback on documentation clarity from end-user stakeholder groups |

---

## Security Lead

### Role Summary
The Security Lead ensures security requirements are defined early, integrated throughout delivery, and met before release. They manage vulnerability assessments, drive incident response, and communicate risk to the team and stakeholders.

### Responsibilities
- Define security requirements and threat models at project initiation
- Integrate security scanning (SAST, DAST, dependency checks) into CI/CD pipelines
- Conduct or coordinate security reviews and penetration testing
- Manage the security incident response process
- Communicate security risks and remediation status to PM, PdM, and leadership
- Maintain the security runbook and incident response playbook
- Ensure compliance with relevant security standards (e.g., SOC 2, OWASP)

### Goals
- Shift security left: catch vulnerabilities early rather than at release
- Reduce mean time to detect and remediate security issues
- Ensure zero critical-severity security findings reach production

### Typical Communication
- Security findings reported in the risk register and issue tracker
- Incident communications drafted and distributed to stakeholders during active incidents
- Security review sign-off as part of the release checklist

### How this role interacts with others
| Interacts With | Collaboration / Handoff |
|---|---|
| Developers | Reviews security-sensitive code changes; advises on secure coding practices; co-owns remediation of vulnerabilities |
| PM | Communicates security risks, timelines for remediation, and escalation needs |
| PdM | Aligns on security requirements and trade-offs during planning; ensures security features are prioritized |
| QA/Testing | Coordinates security test cases; shares scan results for tracking |
| Technical Writer | Collaborates on security advisories, incident communications, and runbook documentation |
| Stakeholder Representative | Communicates risk posture and incident status to stakeholder groups as appropriate |

---

## Business Analyst

### Role Summary
Business Analysts bridge business needs and technical delivery. They translate stakeholder requirements into well-defined, actionable work items that Developers and PdM can prioritize and build effectively.

### Responsibilities
- Elicit and document business requirements through stakeholder interviews and workshops
- Translate requirements into user stories, process flows, and acceptance criteria
- Model and document current-state and future-state business processes
- Identify gaps between stakeholder needs and proposed solutions
- Support backlog refinement and prioritization with PdM
- Validate delivered features against original business requirements

### Goals
- Ensure delivered solutions solve the right business problems
- Reduce rework caused by incomplete or misunderstood requirements
- Maintain a clear traceability from business need to delivered feature

### Typical Communication
- Requirements documents and user story write-ups shared in the project repo
- Active participation in backlog refinement and planning sessions
- Regular check-ins with stakeholders and PdM to validate priorities

### How this role interacts with others
| Interacts With | Collaboration / Handoff |
|---|---|
| PdM | Partners on requirements definition and backlog prioritization; translates business needs into product features |
| PM | Provides requirements documentation as input to the project plan; flags scope changes |
| Developers | Clarifies requirements during implementation; reviews delivered features for business requirement compliance |
| UX/UI Designer | Shares user research and requirements to inform design; reviews designs against business rules |
| Stakeholder Representative | Conducts requirements workshops; documents and validates stakeholder needs |
| QA/Testing | Provides acceptance criteria and business rules for test case design |

---

## Stakeholder Representative

### Role Summary
Stakeholder Representatives act as the voice of key stakeholder groups — customers, support, sales, legal, or finance — within the project team. They ensure stakeholder priorities are understood, communicated, and considered in project decisions.

### Responsibilities
- Represent the interests and priorities of their stakeholder group within the project
- Gather and synthesize feedback from stakeholders during reviews and demos
- Communicate project decisions, timelines, and impacts back to their stakeholder group
- Participate in key project milestones: kickoff, reviews, UAT, release announcements
- Escalate stakeholder concerns to PM or PdM when needed
- Approve deliverables on behalf of their stakeholder group where designated

### Goals
- Ensure stakeholder needs are reflected in product decisions
- Maintain stakeholder confidence and alignment throughout the project
- Reduce late-stage surprises by keeping stakeholders engaged and informed

### Typical Communication
- Attendance at sprint reviews and milestone demos
- Stakeholder group briefings after key project events
- Formal sign-off or approval emails for gated deliverables

### How this role interacts with others
| Interacts With | Collaboration / Handoff |
|---|---|
| PdM | Provides stakeholder input on priorities and validates roadmap direction |
| PM | Receives project status updates; escalates concerns and approval needs |
| Business Analyst | Participates in requirements workshops; validates documented requirements |
| UX/UI Designer | Reviews prototypes and provides user feedback before design is finalized |
| Technical Writer | Reviews user-facing documentation for clarity and completeness before release |
| Security Lead | Receives risk communications and incident updates relevant to their stakeholder group |

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- For a quick overview of which roles are engaged at each project phase, see the [RACI & Handoffs guide](octoacme-raci-and-handoffs.md).

