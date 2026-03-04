# OctoAcme — RACI & Handoffs Guide

## Purpose
Provide lightweight accountability templates and handoff checklists to reduce gaps, duplication, and missed responsibilities across project phases. Use these in combination with the full role definitions in [OctoAcme Roles & Personas](octoacme-roles-and-personas.md).

---

## RACI-Lite Template

**Legend:** R = Responsible | A = Accountable | C = Consulted | I = Informed

Copy this table and fill in R/A/C/I for your project. Remove rows not applicable to your project type.

| Activity | PM | PdM | Dev | QA | UX | TW | Security Lead | BA | Stakeholder Rep |
|---|---|---|---|---|---|---|---|---|---|
| Define problem statement & success metrics | C | A/R | I | I | C | I | C | R | C |
| Stakeholder identification & alignment | R | C | I | I | I | I | I | R | A |
| Requirements elicitation & documentation | C | A | I | I | C | I | C | R | C |
| Backlog creation & prioritization | C | A/R | C | C | C | C | C | R | I |
| UX research & design specs | I | C | C | I | A/R | I | I | C | C |
| Security requirements & threat model | C | C | C | I | I | I | A/R | C | I |
| Documentation scoping & planning | C | C | I | I | I | A/R | I | I | I |
| Sprint/iteration planning | A/R | C | R | C | C | C | I | C | I |
| Feature implementation | I | I | A/R | I | I | I | C | I | I |
| Code review | I | I | A/R | I | I | I | C | I | I |
| Security scanning & remediation | C | I | R | C | I | I | A/R | I | I |
| QA / test execution | C | I | C | A/R | C | I | C | I | I |
| UX / usability review | I | C | I | C | A/R | I | I | I | C |
| Release notes authoring | C | C | C | C | I | A/R | C | I | I |
| Release go/no-go decision | A | C | C | C | C | C | C | I | I |
| Stakeholder communications | R | C | I | I | I | C | C | I | A |
| Post-release incident response | C | I | R | C | I | C | A/R | I | C |
| Retrospective facilitation | A/R | C | C | C | C | C | C | C | C |
| Action item tracking | A/R | C | C | C | C | C | C | C | I |

> **How to use:** Copy this table into your project's planning doc. Tailor rows to your project activities and confirm R/A/C/I assignments with the team during kickoff.

---

## Handoff Checklists

### PdM → Developer Handoff (Feature Ready for Development)
- [ ] User story written with clear title, description, and business context
- [ ] Acceptance criteria defined and reviewed with QA
- [ ] UX/UI design spec linked or attached (if applicable)
- [ ] Business Analyst has reviewed requirements for completeness
- [ ] Security requirements or constraints called out (if applicable)
- [ ] Dependencies on other teams or services identified
- [ ] Story estimated and prioritized in the active sprint/iteration

### Developer → QA Handoff (Feature Ready for Testing)
- [ ] Feature branch merged to agreed integration branch
- [ ] CI passes (tests, lint, security scan)
- [ ] Unit and integration tests written and passing
- [ ] Self-tested against acceptance criteria
- [ ] PR description includes context and test instructions
- [ ] Known limitations or edge cases documented in the issue/PR
- [ ] UX/UI Designer has reviewed implemented UI (if applicable)
- [ ] Security Lead has reviewed security-sensitive changes (if applicable)

### QA → PM Handoff (Feature Ready for Release)
- [ ] All test cases executed; results documented
- [ ] No open blocker or critical defects
- [ ] Regression suite passes
- [ ] Acceptance criteria verified and signed off
- [ ] Usability check completed (UX/UI Designer sign-off where applicable)
- [ ] Security scan results reviewed and approved by Security Lead
- [ ] QA sign-off recorded in the project board or issue tracker

### PM → Stakeholders Handoff (Release Communication)
- [ ] Release notes finalized by Technical Writer and reviewed by PM/PdM
- [ ] Stakeholder Representatives briefed before public announcement
- [ ] Deployment window communicated to relevant teams (support, ops)
- [ ] Release announcement sent (email, Slack, or agreed channel)
- [ ] Post-release monitoring plan shared with on-call teams
- [ ] Feedback channel confirmed for post-release stakeholder input

---

## Role Engagement Checklist by Phase

Use this checklist to ensure the right roles are engaged at each project phase.

### Initiation
- [ ] PM: owns One-pager and stakeholder alignment
- [ ] PdM: validates business need and success metrics
- [ ] Business Analyst: conducts stakeholder interviews; documents requirements context
- [ ] Stakeholder Representative: confirms priorities; reviews One-pager
- [ ] Security Lead: flags initial security/compliance requirements
- [ ] UX/UI Designer: scopes any discovery/research work needed

### Planning
- [ ] PM: owns project plan, timeline, milestones
- [ ] PdM: leads backlog prioritization; defines acceptance criteria
- [ ] Business Analyst: translates requirements into user stories; facilitates refinement
- [ ] UX/UI Designer: delivers wireframes/specs; identifies UX risks
- [ ] Security Lead: defines security requirements; configures CI/CD scanning
- [ ] Technical Writer: scopes documentation; adds doc tasks to backlog
- [ ] Developers: estimate effort; identify technical risks
- [ ] QA/Testing: drafts test plan; contributes to Definition of Done
- [ ] Stakeholder Representative: reviews and approves planned scope

### Execution
- [ ] PM: tracks progress; manages risks; facilitates standups
- [ ] PdM: clarifies requirements; adjusts priorities
- [ ] Developers: implement features; write tests; participate in reviews
- [ ] QA/Testing: executes tests; tracks defects
- [ ] UX/UI Designer: reviews UI fidelity; unblocks design questions
- [ ] Security Lead: monitors security scans; manages vulnerabilities
- [ ] Business Analyst: validates delivered features against requirements
- [ ] Technical Writer: drafts release notes; tracks documentation tasks
- [ ] Stakeholder Representative: attends sprint reviews; provides feedback

### Release
- [ ] PM: owns release go/no-go decision; coordinates deployment window
- [ ] PdM: confirms release scope and stakeholder readiness
- [ ] Security Lead: signs off on security scan results
- [ ] Technical Writer: finalizes and publishes release notes
- [ ] UX/UI Designer: completes usability review sign-off
- [ ] QA/Testing: confirms final test sign-off
- [ ] Stakeholder Representative: receives briefing before public announcement

### Retrospective
- [ ] PM: facilitates retrospective; owns action item tracking
- [ ] All core roles: participate and contribute retrospective input
- [ ] UX/UI Designer, Technical Writer, Security Lead, BA, Stakeholder Rep: invited when their phase contributions are being reviewed
- [ ] Action items assigned with owners and due dates
- [ ] Previous action items reviewed for progress
