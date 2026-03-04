# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans — **Security Lead** provides sign-off
- Release notes drafted and reviewed — owned by **Technical Writer**, reviewed by PM and PdM
- UX/UI Designer has completed usability review and signed off on the release
- Rollback / mitigation plan documented
- Smoke tests prepared

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Security Lead has signed off on security scan results
- [ ] Technical Writer has finalized and published release notes
- [ ] UX/UI Designer has completed usability review
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support (PM + Stakeholder Representatives)

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:

> **Note:** Release notes are owned by the **Technical Writer**. See [OctoAcme Roles & Personas](octoacme-roles-and-personas.md) for the Technical Writer's release responsibilities. For role accountability across the release phase, see the [RACI & Handoffs guide](octoacme-raci-and-handoffs.md).
