# OctoAcme — Role Interactions & Handoffs

## Purpose
Provide a quick-reference guide that maps each lifecycle stage to the roles responsible for it, defines handoff points and required artifacts, and clarifies the escalation path. Use this alongside `octoacme-roles-and-personas.md` to reduce ambiguity and improve cross-functional collaboration.

The matrix below uses **RACI** notation — a lightweight accountability framework where each role is classified as **Responsible** (does the work), **Accountable** (owns the outcome), **Consulted** (provides input), or **Informed** (kept up to date).

---

## Lifecycle Stage × Role Matrix (RACI)

> **Legend:** R = Responsible | A = Accountable | C = Consulted | I = Informed

| Lifecycle Stage | Project Manager (PM) | Product Manager (PdM) | Developers | QA Lead | Release Manager | UX Designer | Support Coordinator | Stakeholders |
|---|---|---|---|---|---|---|---|---|
| **Initiation** | A/R | A/R | C | I | I | C | I | C/I |
| **Planning** | A/R | A/R | R | R | C | R | C | C/I |
| **Execution** | A | R | R | R | I | R | I | I |
| **Release** | A | C | R | R (sign-off) | A/R | C | R | I |
| **Retrospective / Incidents** | A/R | C | R | R | R | C | R | I |

---

## Handoff Points & Required Artifacts

### 1. Initiation → Planning

**Trigger:** Project charter / one-pager approved by stakeholders.

**Handoff from:** Project Manager + Product Manager  
**Handoff to:** Full delivery team (Developers, QA Lead, UX Designer, Release Manager, Support Coordinator)

**Required artifacts / sign-offs:**
- [ ] Project Charter / One-pager reviewed and approved
- [ ] High-level goals and success metrics defined
- [ ] Initial stakeholder list confirmed
- [ ] UX Designer briefed on scope and early user constraints
- [ ] QA Lead notified so initial test strategy can be drafted in Planning

---

### 2. Planning → Execution

**Trigger:** Kickoff meeting held; backlog, Definition of Done, and release milestones agreed.

**Handoff from:** Project Manager + Product Manager  
**Handoff to:** Developers, QA Lead, UX Designer

**Required artifacts / sign-offs:**
- [ ] Prioritized backlog with acceptance criteria (see `octoacme-project-planning.md`)
- [ ] Definition of Done documented
- [ ] Initial test plan / QA approach drafted (QA Lead sign-off)
- [ ] UX wireframes / user flows for in-scope features shared with Developers
- [ ] Release plan and milestone map reviewed by Release Manager
- [ ] Risk Register initialized (see `octoacme-risks-and-communication.md`)
- [ ] Support Coordinator briefed on upcoming changes

---

### 3. Execution → Release (Code-Freeze / Release Gate)

**Trigger:** All acceptance criteria met; QA sign-off received; Release Manager declares code-freeze.

**Handoff from:** Developers + QA Lead  
**Handoff to:** Release Manager

**Required artifacts / sign-offs:**
- [ ] All PRs merged; CI green; security scans passed
- [ ] Acceptance criteria validated and QA Lead sign-off recorded
- [ ] Release notes drafted by Release Manager
- [ ] Rollback / mitigation plan documented (see `octoacme-release-and-deployment.md`)
- [ ] Smoke tests prepared and reviewed with QA Lead
- [ ] Support runbooks and FAQs prepared by Support Coordinator
- [ ] Deployment window scheduled and communicated

---

### 4. Release → Retrospective / Monitoring

**Trigger:** Deployment to production complete; post-deploy verification passed.

**Handoff from:** Release Manager  
**Handoff to:** Support Coordinator + full team (for retrospective)

**Required artifacts / sign-offs:**
- [ ] Post-deploy verification checklist complete (see `octoacme-release-and-deployment.md`)
- [ ] Release announced to stakeholders and support team
- [ ] Support Coordinator begins post-release monitoring
- [ ] Retrospective scheduled (see `octoacme-retrospective-and-continuous-improvement.md`)
- [ ] Deployment metrics and incident data captured by Release Manager

---

## Escalation & Support Path

This path aligns with `octoacme-execution-and-tracking.md` and `octoacme-risks-and-communication.md`.

```
Team-level triage (daily standup)
    ↓
Project Manager (PM) — escalates to Product Lead and dependent teams
    ↓
Product Lead — business prioritization and resource decisions
    ↓
Sponsor — business-impacting or budget-level decisions
```

**Security / On-call path:**
- For security incidents: follow the security incident runbook and notify Security on-call immediately; PM and Product Lead are informed in parallel.
- For production incidents: Support Coordinator triggers incident response, notifies Release Manager and Developers; PM manages stakeholder communication using the incident template from `octoacme-risks-and-communication.md`.

---

## Quick-Reference: Who to Contact at Each Stage

| Question / Need | Primary Contact | Backup / Escalation |
|---|---|---|
| Scope or priority change | Product Manager (PdM) | Project Manager (PM) |
| Schedule or dependency conflict | Project Manager (PM) | Product Manager (PdM) |
| Technical feasibility or implementation | Developers | Project Manager (PM) |
| Test coverage or quality gate | QA Lead | Project Manager (PM) |
| Release scheduling or deployment | Release Manager | Project Manager (PM) |
| Design or usability question | UX Designer | Product Manager (PdM) |
| Post-release user issue or bug triage | Support Coordinator | Project Manager (PM) |
| Risk or stakeholder communication | Project Manager (PM) | Product Manager (PdM) |
