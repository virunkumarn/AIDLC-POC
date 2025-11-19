# 2.3 Implementation

**Objective**: Generate working code based on logical design specifications
**Focus**: Domain models, API endpoints, data access, integration components

## Entry Point Requirements
**Can start this phase if:**
- [ ] `user-stories.md` exists from phase 1.1
- [ ] `domain-decomposition.md` exists from phase 1.2
- [ ] Domain design completed for target context (from phase 2.1)
- [ ] Logical design completed for target context (from phase 2.2)
- [ ] Technical specifications and technology choices defined

**Missing Prerequisites Handling:**
- Guide user to complete missing phases first
- Validate logical design completeness before proceeding
- Ensure all technical specifications are defined

## Required Context from Previous Phases

- **From 1.1**: User stories for feature validation from `user-stories.md`
- **From 1.2**: Architecture pattern and integration requirements from `domain-decomposition.md`
- **From 2.1**: Domain model specifications from `domain_design.md`
- **From 2.2**: Technical specifications and technology choices from `logical_design.md`

## Process

### Azure DevOps Integration Workflow

1. **Ticket Selection**
   - Ask user which Azure DevOps work item/ticket number to implement
   - Validate ticket exists and contains sufficient implementation details
   - Review ticket description, acceptance criteria, and linked requirements

2. **Update Ticket Status to In-Progress**
   - Update the selected work item status to "In-Progress" in Azure DevOps
   - Ensure ticket is assigned to the appropriate developer
   - Link ticket to current sprint/iteration if applicable

3. **Implementation Phase**
   - **MANDATORY**: Use the implementation plan template at `.amazonq/templates/planning/implementation-plan-template.md` for systematic implementation
   - **MANDATORY**: Map all MVP user stories from phase 1.1 to implementation tasks
   - Apply local-first development approach
   - Implement MVP scope first, then plan future features
   - Ensure testable and runnable components
   - Follow coding standards and SOLID principles
   - Write unit tests and integration tests as code is developed

4. **Testing and Validation**
   - Run all unit tests and ensure they pass
   - Execute integration tests to verify end-to-end functionality
   - Validate against ticket acceptance criteria
   - Test user workflows per user story requirements
   - Ensure application runs locally without errors

5. **Create Pull Request**
   - After coding and testing are complete, create a pull request in Azure DevOps
   - Ensure PR title references the work item number (e.g., "AB#123: Implement user authentication")
   - Include comprehensive PR description with:
     - Summary of changes
     - Reference to work item/ticket
     - Testing performed
     - Screenshots/demos if applicable
   - Link PR to the work item in Azure DevOps

6. **Update Ticket Status to Code Review**
   - Once PR is created, update work item status to "Code Review"
   - Add PR link to work item comments
   - Notify reviewers and stakeholders
   - Address review feedback and update PR as needed

## User Story Traceability Requirements

### Before Creating Implementation Plan:
1. **Review user-stories.md** from phase 1.1 requirements gathering
2. **Identify MVP user stories** that must be implemented
3. **Map each user story** to specific implementation tasks
4. **Validate completeness** - ensure no MVP stories are missed

### During Implementation:
- **Reference user stories** in each task description
- **Validate acceptance criteria** for each implemented story
- **Frontend implementation** reference from `templates/frontend-template` styles, look & feels and UX/UI pattern
- **Test user workflows** end-to-end per story
- **Update story status** as implementation progresses

## Implementation Priority

1. **User Story Driven**: Implement features that complete user stories end-to-end
2. **Local-First**: Implement for local development first (in-memory storage, console logging)
3. **MVP Focus**: Implement only what's needed to satisfy MVP user stories
4. **Feature-Complete**: Each implementation phase should complete specific user stories
5. **Testable**: Ensure each user story can be validated independently

## Phase Transition Validation

Before proceeding to Operation phase (3.1), validate:

- [ ] All MVP user stories from phase 1.1 are implemented
- [ ] Each user story's acceptance criteria are met
- [ ] User workflows are complete and testable
- [ ] Application runs locally without errors
- [ ] All implemented features have been validated
- [ ] **User story traceability** is complete and documented

## Post-MVP Planning

After MVP completion, create implementation plan for future features:
- Review "Future" scope items from logical design (step 2.2)
- Review post-MVP user stories from requirements (step 1.1)
- Prioritize post-MVP features based on business value
- Create implementation roadmap with phases
- Document technical debt and refactoring needs
- Plan integration points for future features
