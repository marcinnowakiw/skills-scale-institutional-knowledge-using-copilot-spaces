# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support
- [ ] Handoff support plan to Support Lead with escalation paths

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call (including Release Manager and Support Lead)
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items in retro
  - Update incident and rollback documentation as needed

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:

## Improving Release & Deployment
- Schedule pre-release signoff involving Release Manager, QA, and Product Manager
- Document lessons learned after every significant release in retro/action tracker
- Review failed releases/incidents in blameless retrospectives

## Continuous Improvement Actions
- Track mean time to release and rollback statistics
- Update deployment checklist as gaps are discovered
- Share release outcomes and improvements in team syncs and docs