# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI — owned by the **Security Lead**, who reviews findings and works with Developers on remediation
- UX/UI Designer performs usability review of implemented features against design specs before QA sign-off
- Manual QA for feature acceptance when needed

## Key Roles at This Phase
| Role | Responsibility during Execution |
|---|---|
| PM | Tracks progress, manages risks, facilitates standups and escalations |
| PdM | Clarifies acceptance criteria; adjusts priorities based on new information |
| Developers | Implement features; write tests; participate in code and design reviews |
| QA/Testing | Executes test plans; validates feature completeness; signs off on quality |
| UX/UI Designer | Reviews implemented UI for design fidelity and usability; unblocks dev on design questions |
| Security Lead | Monitors security scan results in CI; manages vulnerability remediation; manages incidents |
| Business Analyst | Validates delivered features against original business requirements |
| Technical Writer | Tracks feature changes with documentation impact; drafts release notes iteratively |

> See [OctoAcme Roles & Personas](octoacme-roles-and-personas.md) for full role definitions.
> Use the [RACI & Handoffs guide](octoacme-raci-and-handoffs.md) for handoff checklists between roles.

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests, lint, and security scanning (Security Lead confirms)
- [ ] Regular demos scheduled (include Stakeholder Representatives and UX/UI Designer)
- [ ] Risk register updated weekly
- [ ] UX/UI Designer performing per-sprint design fidelity reviews
- [ ] Technical Writer tracking feature changes for documentation updates
