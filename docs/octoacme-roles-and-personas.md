# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

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

## Release Manager

### Role Summary
Release Managers plan, coordinate, and gate all software releases. They own the release process from code-freeze through post-deployment verification, ensuring every release meets quality and readiness standards before reaching production.

### Responsibilities
- Define and maintain the release plan, schedule, and milestones
- Enforce release gates (all acceptance criteria met, CI green, security scans passed)
- Draft and publish release notes and deployment runbooks
- Coordinate deployment windows with Developers, QA Lead, and infrastructure owners
- Manage rollback plans and trigger incident response when a release fails
- Communicate release status to stakeholders and Support Coordinator

### Goals
- Ship reliable, well-documented releases on schedule
- Reduce deployment risk through consistent process and automation
- Keep stakeholders informed before, during, and after each release

### Typical Communication
- Release readiness reviews with PM, QA Lead, and Developers
- Pre-release announcements to stakeholders and support teams
- Post-release retrospective notes capturing deployment metrics

### Lifecycle Participation & Role Interactions
- **Planning:** Collaborates with Project Manager and Product Manager to define release milestones and scope boundaries.
- **Execution:** Works with Developers to track merge readiness and with QA Lead to confirm test sign-off before code-freeze.
- **Release:** Drives the deployment checklist (see `octoacme-release-and-deployment.md`), owns go/no-go decisions, and coordinates smoke testing with QA Lead.
- **Retrospective:** Provides deployment metrics and incident data for the retrospective; captures action items around release process improvements.

---

## QA Lead

### Role Summary
The QA Lead owns quality strategy across the entire project lifecycle. They design test plans, coordinate manual and automated testing, and ensure that acceptance criteria are fully validated before a release is approved.

### Responsibilities
- Define the overall test strategy and quality standards
- Create and maintain test plans, test cases, and acceptance checklists
- Coordinate manual and automated testing (unit, integration, end-to-end, smoke)
- Validate that each story/feature meets its acceptance criteria and the Definition of Done
- Provide sign-off to the Release Manager before deployment
- Identify quality risks and escalate blockers to the Project Manager

### Goals
- Achieve thorough, repeatable test coverage for every release
- Catch defects early to reduce the cost of fixes
- Continuously improve testing practices through retrospective feedback

### Typical Communication
- Sprint planning and kickoff with Developers and Product Manager to clarify acceptance criteria
- Daily or as-needed sync with Developers on defects and test status
- Release readiness sign-off with Release Manager
- Retrospective notes on quality metrics (defect rate, test coverage)

### Lifecycle Participation & Role Interactions
- **Planning:** Partners with Product Manager to review acceptance criteria; contributes the initial test plan/QA approach to the planning checklist (see `octoacme-project-planning.md`).
- **Execution:** Participates in code reviews and demos; tracks defects on the project board; escalates blocking bugs to Project Manager.
- **Release:** Performs final acceptance testing and issues go/no-go sign-off to the Release Manager.
- **Retrospective:** Reports quality metrics and proposes test automation improvements.

---

## UX Designer

### Role Summary
UX Designers translate product requirements into user flows, wireframes, and interactive prototypes. They advocate for user-centric design throughout the project lifecycle and validate that delivered features meet usability standards.

### Responsibilities
- Collaborate with Product Manager to understand user needs and define experience goals
- Produce user flows, wireframes, and high-fidelity mockups for features in scope
- Facilitate usability reviews and incorporate feedback iteratively
- Work with Developers to ensure design feasibility and implementation fidelity
- Provide design acceptance criteria so QA Lead can validate usability
- Contribute UX findings and usability metrics to retrospectives

### Goals
- Deliver intuitive, accessible experiences aligned with product goals
- Reduce re-work by involving design early and maintaining a shared design language
- Increase user satisfaction as measured by usability scores and feedback

### Typical Communication
- Design reviews with Product Manager and Developers during Planning and early Execution
- Handoff notes and annotated mockups shared with Developers before implementation begins
- Usability test results shared with Product Manager and Project Manager
- Participation in sprint demos to confirm implementation matches design intent

### Lifecycle Participation & Role Interactions
- **Initiation:** Reviews the problem statement with Product Manager and identifies early UX constraints or risks.
- **Planning:** Delivers wireframes and user flows needed for backlog refinement; works with Product Manager on acceptance criteria that include usability requirements.
- **Execution:** Provides ongoing design guidance to Developers; reviews PRs or demos for design fidelity; coordinates with QA Lead on usability testing criteria.
- **Release:** Reviews release notes and communication materials to confirm user-facing language is clear.
- **Retrospective:** Shares usability findings and user feedback collected post-release.

---

## Support Coordinator

### Role Summary
Support Coordinators act as the bridge between users/customers and the project team. They triage incoming bugs and incidents post-release, ensure that user feedback flows back into planning, and coordinate resolution timelines with the delivery team.

### Responsibilities
- Monitor support channels and triage incoming user issues and incidents after release
- Reproduce and document bugs with enough detail for Developer investigation
- Escalate critical incidents to the Project Manager and trigger the incident runbook (see `octoacme-release-and-deployment.md`)
- Track resolution progress and communicate status updates to affected users
- Aggregate user feedback and pain points and present them to Product Manager and Project Manager
- Participate in retrospectives to surface patterns from support data

### Goals
- Minimize user impact from post-release issues through fast triage and clear escalation
- Close the feedback loop between users and the product team to inform future planning
- Build user trust through timely, transparent communication

### Typical Communication
- Regular sync with Product Manager to review open support themes and feedback
- Incident status updates to stakeholders using the communication template from `octoacme-risks-and-communication.md`
- Post-incident retrospective participation to share root-cause context
- Coordination with Release Manager before releases to prepare support runbooks and FAQs

### Lifecycle Participation & Role Interactions
- **Planning:** Reviews upcoming changes with Product Manager to anticipate support impact; prepares FAQs and support runbooks.
- **Release:** Works with Release Manager to confirm support materials are ready; stands by for post-release monitoring.
- **Retrospective/Incidents:** Brings user and support data into retrospectives; collaborates with Developers on hotfix prioritization; follows the escalation path (Team → PM → Product Lead → Sponsor) defined in `octoacme-execution-and-tracking.md`.

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

