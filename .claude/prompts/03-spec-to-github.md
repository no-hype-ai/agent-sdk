# Specification to GitHub Epic Transformation Prompt

## Objective

Transform validated specifications into actionable GitHub epics, issues, and project structures that enable 11x development velocity through optimal task orchestration and parallel execution patterns.

## Epic Creation Framework

### Step 1: Epic Structure Generation

#### Epic Metadata Creation
```markdown
**Epic Title**: [Business-focused, outcome-oriented]
- Format: "Enable [user capability] through [technical solution]"
- Example: "Enable autonomous task execution through OpenHands SDK integration"

**Epic Description Template**:
```
## Business Objective
[Clear value proposition and user impact]

## Technical Approach  
[High-level implementation strategy with SDK-first focus]

## Success Criteria
[Measurable outcomes from validated specification]

## Implementation Phases
[4-phase progressive enhancement structure]

## Dependencies & Prerequisites
[Clear blocking and enabling relationships]

## Risk Assessment
[Key risks and mitigation strategies]
```

#### Phase Structure Mapping
```python
# Map specification phases to GitHub epic structure
EPIC_PHASE_MAPPING = {
    "Phase 1: Foundation (Weeks 1-2)": {
        "focus": "Essential functionality only",
        "complexity_limit": "S/M issues only",
        "parallel_streams": ["backend_setup", "database_schema", "basic_auth"],
        "deliverables": ["MVP API", "Database foundation", "Authentication"]
    },
    "Phase 2: Core Features (Weeks 3-4)": {
        "focus": "Primary feature implementation",
        "complexity_limit": "M issues, limited L",
        "parallel_streams": ["feature_implementation", "testing_suite", "documentation"],
        "deliverables": ["Core functionality", "Test coverage", "API docs"]
    },
    "Phase 3: Integration (Weeks 5-6)": {
        "focus": "External integrations and collaboration",
        "complexity_limit": "M/L issues",
        "parallel_streams": ["external_apis", "ui_integration", "monitoring"],
        "deliverables": ["External integrations", "UI components", "Monitoring"]
    },
    "Phase 4: Production (Weeks 7-8)": {
        "focus": "Production readiness and optimization",
        "complexity_limit": "L issues for infrastructure",
        "parallel_streams": ["security_hardening", "performance_optimization", "deployment"],
        "deliverables": ["Security validation", "Performance targets", "Deployment automation"]
    }
}
```

### Step 2: Issue Generation Strategy

#### Issue Decomposition Framework
```markdown
**Issue Creation Rules**:
1. **Single Responsibility**: Each issue addresses one specific deliverable
2. **File-Based Separation**: Issues that modify different files can run in parallel
3. **Layer Separation**: Frontend, backend, database, and infrastructure issues separate
4. **Testing Independence**: Test issues parallel to implementation where possible
5. **Documentation Parallel**: Documentation issues run alongside implementation

**Issue Size Guidelines** (Enforced):
- **Small (S)**: 1-3 days, single file or component modification
- **Medium (M)**: 3-5 days, multiple related files or integration work  
- **Large (L)**: 5-10 days, complex integration or infrastructure (rare, justify necessity)
- **XL**: FORBIDDEN - must be decomposed into smaller issues
```

#### Parallelization Opportunity Analysis
```python
# Framework for identifying parallel execution opportunities
PARALLEL_EXECUTION_ANALYSIS = {
    "file_separation": {
        "backend_api": ["src/apps/api-service/", "tests/api/"],
        "frontend_components": ["src/apps/web-app/src/", "src/libs/frontend/"],
        "database_migrations": ["src/apps/api-service/migrations/"],
        "documentation": ["docs/", "README.md"],
        "infrastructure": ["deploy/", "scripts/", ".github/"]
    },
    "layer_separation": {
        "data_layer": "Database schema, models, migrations",
        "business_layer": "API endpoints, business logic, validation",
        "presentation_layer": "UI components, forms, user flows",
        "integration_layer": "External APIs, webhooks, event handling"
    },
    "testing_streams": {
        "unit_tests": "Parallel with implementation",
        "integration_tests": "Parallel with API development",
        "e2e_tests": "Parallel with UI development", 
        "security_tests": "Parallel with authentication work"
    }
}
```

### Step 3: GitHub Project Structure Creation

#### Project Board Configuration
```markdown
**Column Structure** (Optimized for flow):
1. **Backlog**: All issues prioritized and ready
2. **Ready**: Issues with no blocking dependencies  
3. **In Progress**: Active work (limit: 3-4 issues per developer)
4. **Review**: Code review and validation in progress
5. **Testing**: Quality assurance and validation
6. **Done**: Completed and validated

**Labels for Orchestration**:
- `epic:phase-1`, `epic:phase-2`, `epic:phase-3`, `epic:phase-4`
- `parallel:backend`, `parallel:frontend`, `parallel:database`, `parallel:docs`
- `size:S`, `size:M`, `size:L` 
- `priority:critical`, `priority:high`, `priority:medium`, `priority:low`
- `type:feature`, `type:bug`, `type:infrastructure`, `type:documentation`
```

#### Milestone & Timeline Structure
```markdown
**Milestone Creation** (Aligned with phases):
```
Milestone: Epic [ID] Phase 1 - Foundation  
Due Date: [2 weeks from start]
Description: Essential functionality and infrastructure foundation
Success Criteria: [Phase 1 deliverables from specification]

Milestone: Epic [ID] Phase 2 - Core Features
Due Date: [4 weeks from start] 
Description: Primary feature implementation and core functionality
Success Criteria: [Phase 2 deliverables from specification]

[Continue for Phases 3 & 4]
```

### Step 4: Issue Template Generation

#### Comprehensive Issue Template
```markdown
**Issue Template Structure**:
```
# [Issue Title] - [Size] [Type]

## Objective
[Clear, specific goal aligned with epic success criteria]

## Implementation Details
- [ ] **Setup**: [Environment, dependencies, prerequisites]
- [ ] **Core Implementation**: [Specific code changes required]
- [ ] **Testing**: [Required test coverage and validation]
- [ ] **Documentation**: [Required documentation updates]

## Technical Requirements
- **Files to Modify**: [Specific file paths]
- **Dependencies**: [Any blocking issues or external dependencies]
- **SDK Integration**: [Specific OpenHands SDK components to use]
- **Database Changes**: [Schema changes, migrations required]

## Acceptance Criteria
- [ ] [Specific, testable criteria from specification]
- [ ] [Performance requirements if applicable]
- [ ] [Security requirements if applicable]
- [ ] [Integration requirements if applicable]

## Testing Requirements
- [ ] Unit tests: [Specific test cases]
- [ ] Integration tests: [API endpoint testing]
- [ ] Manual testing: [User workflow validation]
- [ ] Performance testing: [If applicable]

## Definition of Done
- [ ] Code implemented and reviewed
- [ ] All tests passing (unit, integration, e2e as applicable)
- [ ] Documentation updated
- [ ] Performance requirements met
- [ ] Security requirements validated
- [ ] Deployment ready (if applicable)

## Parallel Work Opportunities
[Other issues that can run in parallel with this one]

## Estimated Effort: [1-3 days (S), 3-5 days (M), 5-10 days (L)]
```

### Step 5: Dependency Graph Generation

#### Dependency Analysis Framework
```python
# Create clear dependency relationships for optimal orchestration
DEPENDENCY_TYPES = {
    "blocking": "Must complete before this issue can start",
    "enabling": "Provides functionality this issue builds upon", 
    "integrating": "Must coordinate with this issue for integration",
    "conflicting": "Cannot run in parallel due to file conflicts"
}

# Dependency mapping strategy
def create_dependency_graph(issues):
    dependencies = {
        "foundation_dependencies": {
            "database_schema": [],  # No dependencies, can start immediately
            "basic_auth": ["database_schema"],  # Needs user table
            "api_framework": []  # Can start in parallel with database
        },
        "feature_dependencies": {
            "core_endpoints": ["database_schema", "basic_auth"],
            "user_management": ["basic_auth", "api_framework"],
            "task_processing": ["api_framework"]  # Can be parallel
        },
        "integration_dependencies": {
            "external_api_integration": ["core_endpoints"],
            "ui_integration": ["core_endpoints", "user_management"],
            "monitoring": []  # Can be parallel throughout
        }
    }
    return dependencies
```

#### Wave Execution Planning
```markdown
**Wave Structure** (Based on dependency analysis):

**Wave 1 - Foundation (Parallel execution possible)**:
- Database schema setup
- API framework initialization  
- Basic authentication system
- Development environment setup
- CI/CD pipeline configuration

**Wave 2 - Core Features (Some parallelization possible)**:
- Core API endpoints (depends on Wave 1)
- User management system (depends on auth)
- Task processing logic (can be parallel)
- Unit testing suite (parallel with implementation)

**Wave 3 - Integration (Parallel streams)**:
- External API integration (depends on Wave 2)
- Frontend integration (depends on Wave 2) 
- Monitoring and alerting (can be parallel)
- Documentation updates (parallel throughout)

**Wave 4 - Production Readiness (Final parallel push)**:
- Security hardening (can be parallel)
- Performance optimization (depends on Wave 3)
- Deployment automation (can be parallel)
- Final testing and validation
```

### Step 6: Quality Gates & Automation Integration

#### Automated Quality Gates
```markdown
**GitHub Actions Integration** (Repository automation):
```yaml
# Quality gates for each issue completion
name: Issue Quality Gate
on:
  pull_request:
    types: [opened, synchronize]

jobs:
  quality_validation:
    runs-on: ubuntu-latest
    steps:
      - name: Code Quality Check
        run: |
          make lint
          make test
          make security-scan
          
      - name: Performance Validation
        run: |
          make performance-test
          
      - name: Documentation Validation  
        run: |
          make docs-check
```

#### Progress Tracking Automation
```markdown
**Automated Epic Progress Updates**:
- Issue completion automatically updates epic progress
- Milestone progress tracked and reported
- Dependency satisfaction monitored
- Parallel work coordination through automated checks
- Quality metrics collected and reported
```

### Step 7: Integration with Epic Commands

#### Command Integration Strategy
```bash
# Commands for GitHub integration and management
/epic create-github-issues <epic-id>     # Generate issues from specification
/epic sync-project-board <epic-id>       # Update project board with current status
/epic dependency-check <epic-id>         # Validate dependency satisfaction
/epic parallel-opportunities <epic-id>   # Identify available parallel work
/epic milestone-progress <epic-id>       # Generate milestone progress report
```

#### Workflow Automation
```markdown
**Epic to GitHub Workflow** (End-to-end automation):
1. Validated specification input
2. Epic structure generation with phases
3. Issue decomposition with parallel analysis
4. GitHub project creation with proper labels/milestones  
5. Dependency graph creation
6. Quality gate configuration
7. Progress tracking automation setup
8. Team notification and assignment coordination
```

## Quality Assurance Framework

### GitHub Structure Validation
```markdown
**Epic Quality Checklist**:
- [ ] Epic title is outcome-focused and business-aligned
- [ ] All phases have clear deliverables and success criteria
- [ ] No XL issues (all decomposed into S/M/L)
- [ ] Parallel execution opportunities identified and labeled
- [ ] Dependencies clearly mapped with no circular dependencies
- [ ] Quality gates configured for all issue types
- [ ] Milestone structure aligns with 4-phase progressive enhancement

**Issue Quality Checklist**:
- [ ] Each issue has single, clear responsibility
- [ ] Acceptance criteria are specific and testable
- [ ] File modification scope clearly defined
- [ ] Testing requirements comprehensive
- [ ] Documentation requirements specified
- [ ] Parallel work opportunities identified
- [ ] Estimated effort realistic for issue size
```

### Success Metrics Integration
```markdown
**GitHub Integration Success Metrics**:
- Epic completion rate: 100% (all issues completed)
- Issue estimation accuracy: 90%+ (actual vs. estimated effort)
- Parallel execution efficiency: 5x+ through orchestration
- Quality gate pass rate: 95%+ (minimal rework required)
- Dependency satisfaction rate: 100% (no blocking issues)

**Reporting Integration**:
- Daily progress reports generated automatically
- Weekly milestone progress summaries
- Issue completion velocity tracking
- Quality metrics dashboard
- Risk identification and mitigation tracking
```

This framework transforms validated specifications into actionable GitHub structures that enable the proven 11x development velocity through optimal orchestration and quality assurance.
