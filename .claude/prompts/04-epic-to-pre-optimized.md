# Epic to Pre-Optimized Execution Preparation Prompt

## Objective

Transform GitHub epics into execution-ready work packages with optimized orchestration patterns, agent assignment strategies, and parallel execution plans that achieve 11x development velocity through proven coordination frameworks.

## Pre-Execution Optimization Framework

### Step 1: Epic Readiness Assessment

#### Epic Maturity Validation
```markdown
**Epic Readiness Checklist** (100% required before optimization):
- [ ] **Specification Completeness**: All technical requirements clearly defined
- [ ] **GitHub Structure**: Epic, issues, milestones, and dependencies properly configured
- [ ] **Issue Quality**: All issues sized S/M/L with clear acceptance criteria  
- [ ] **Dependency Mapping**: Complete dependency graph with no circular dependencies
- [ ] **Parallel Opportunities**: All parallel execution streams identified
- [ ] **Quality Gates**: Automated validation configured for all issue types
- [ ] **Resource Requirements**: Development resource needs estimated and validated

**Epic Complexity Assessment**:
```python
EPIC_COMPLEXITY_SCORING = {
    "total_issues": "Number of issues (target: ≤32 for 2-week epic)",
    "dependency_depth": "Longest dependency chain (target: ≤4 levels)",
    "parallel_streams": "Number of independent parallel paths (target: 4-6)",
    "external_dependencies": "Third-party integrations required (target: minimize)",
    "technical_unknowns": "Unresolved technical questions (target: 0)"
}

# Target Score: 85+ for optimal execution readiness
```

#### Resource Optimization Analysis
```markdown
**Development Resource Mapping**:
- **Backend Specialists**: API development, database design, business logic
- **Frontend Specialists**: UI components, user experience, integration
- **Infrastructure Specialists**: CI/CD, deployment, monitoring, security
- **Quality Assurance**: Testing strategy, validation, performance verification
- **Integration Specialists**: External APIs, system integration, data flow

**Agent Assignment Strategy** (Based on proven patterns):
```python
OPTIMAL_AGENT_ASSIGNMENT = {
    "phase_implementer": {
        "specialization": "Backend API development, business logic",
        "optimal_issues": ["database_operations", "api_endpoints", "business_rules"],
        "parallel_capacity": "2-3 issues simultaneously",
        "handoff_points": "API contracts defined, database schema ready"
    },
    "precommit_compliance_reviewer": {
        "specialization": "Code quality, testing, standards compliance",
        "optimal_issues": ["testing_suites", "code_quality", "documentation"],
        "parallel_capacity": "Continuous review across all streams",
        "handoff_points": "Implementation completed, ready for review"
    },
    "issue_validator": {
        "specialization": "Requirements validation, acceptance criteria verification",
        "optimal_issues": ["feature_validation", "integration_testing", "user_acceptance"],
        "parallel_capacity": "1-2 validation streams",
        "handoff_points": "Feature implementation complete"
    }
}
```

### Step 2: Orchestration Strategy Design

#### Wave-Based Execution Planning
```markdown
**Wave Execution Strategy** (Optimized for parallel efficiency):

**Wave 1: Foundation Parallel Stream** (Week 1)
```python
WAVE_1_OPTIMIZATION = {
    "parallel_streams": {
        "infrastructure": ["CI/CD setup", "Docker configuration", "database setup"],
        "backend_foundation": ["API framework", "authentication", "basic models"],
        "frontend_foundation": ["UI framework", "routing", "basic components"],
        "documentation": ["API documentation setup", "development guides"]
    },
    "coordination_points": [
        "End of Week 1: All foundation components ready for integration"
    ],
    "parallel_efficiency": "4x speedup through independent foundation work"
}
```

**Wave 2: Feature Development Parallel Stream** (Week 2)
```python
WAVE_2_OPTIMIZATION = {
    "parallel_streams": {
        "core_features": ["Primary business logic", "main API endpoints"],
        "testing_development": ["Unit tests", "integration tests"],
        "ui_development": ["User interfaces", "user workflows"], 
        "integration_prep": ["External API setup", "data validation"]
    },
    "coordination_points": [
        "Mid-Week 2: Core features ready for testing integration",
        "End of Week 2: All features implemented and validated"
    ],
    "parallel_efficiency": "3.5x speedup through feature stream coordination"
}
```

#### Conflict Avoidance Strategy
```markdown
**File-Level Conflict Prevention**:
```python
FILE_CONFLICT_ANALYSIS = {
    "backend_files": {
        "safe_parallel": ["different_modules", "separate_endpoints", "independent_models"],
        "conflict_risk": ["shared_models", "common_utilities", "configuration_files"],
        "mitigation": "Assign shared files to single agent, define clear interfaces"
    },
    "frontend_files": {
        "safe_parallel": ["separate_components", "different_pages", "independent_styles"],
        "conflict_risk": ["shared_components", "global_styles", "routing_configuration"],
        "mitigation": "Component-based assignment, style guideline enforcement"
    },
    "configuration_files": {
        "high_conflict": ["package.json", "requirements.txt", "docker-compose.yml"],
        "assignment_strategy": "Single agent ownership with coordination checkpoints"
    }
}
```

### Step 3: Agent Specialization Optimization

#### Capability-Based Assignment
```markdown
**Agent Specialization Matrix** (Proven efficiency patterns):

**phase-implementer** (Backend Focus):
- **Optimal Tasks**: Database schema, API endpoints, business logic, data processing
- **Parallel Capacity**: 2-3 related backend issues simultaneously
- **Quality Focus**: Code structure, performance, data integrity
- **Handoff Specialization**: Clean API contracts, comprehensive error handling

**precommit-compliance-reviewer** (Quality Focus):
- **Optimal Tasks**: Code review, testing strategy, compliance validation, documentation
- **Parallel Capacity**: Continuous review across all development streams
- **Quality Focus**: Standards compliance, test coverage, security validation
- **Handoff Specialization**: Quality gates passed, comprehensive validation

**build-reviewer** (Infrastructure Focus):
- **Optimal Tasks**: CI/CD pipelines, Docker configuration, deployment automation
- **Parallel Capacity**: Infrastructure tasks across all development phases
- **Quality Focus**: Deployment reliability, security configuration, monitoring
- **Handoff Specialization**: Production-ready deployment processes

**spec-analyzer** (Analysis & Documentation):
- **Optimal Tasks**: Requirements analysis, documentation, integration planning
- **Parallel Capacity**: Analysis and documentation parallel to development
- **Quality Focus**: Specification accuracy, comprehensive documentation
- **Handoff Specialization**: Clear requirements, complete documentation
```

#### Load Balancing Strategy
```python
# Optimal workload distribution based on agent capabilities
AGENT_LOAD_OPTIMIZATION = {
    "capacity_planning": {
        "phase_implementer": {
            "concurrent_issues": 2-3,
            "issue_types": ["Medium complexity backend tasks"],
            "coordination_overhead": "Low (independent modules)"
        },
        "precommit_compliance_reviewer": {
            "concurrent_reviews": "All active streams",
            "review_types": ["Code quality", "Testing", "Standards"],
            "coordination_overhead": "Medium (cross-stream coordination)"
        }
    },
    "workload_balancing": {
        "prevent_overload": "No agent assigned >75% capacity",
        "maintain_quality": "Quality agents not overloaded with volume",
        "enable_flexibility": "Reserve 25% capacity for priority shifts"
    }
}
```

### Step 4: Quality Gate Pre-Configuration

#### Automated Quality Validation
```markdown
**Quality Gate Configuration** (Pre-execution setup):

**Code Quality Gates**:
```yaml
# Automated quality validation for all pull requests
quality_gates:
  linting:
    python: "ruff check --fix"
    typescript: "biome check --apply"
    
  testing:
    unit_tests: "pytest tests/ --cov=90"
    integration_tests: "pytest tests/integration/"
    
  security:
    dependency_scan: "safety check"
    code_scan: "bandit -r src/"
    
  performance:
    load_testing: "locust --host=localhost:8000"
    response_time: "API responses <200ms"
```

**Integration Quality Gates**:
- **API Contract Validation**: OpenAPI spec compliance verification
- **Database Schema Validation**: Migration testing and rollback verification  
- **Authentication Testing**: Security flow validation and token handling
- **External Integration Testing**: Third-party API connection and error handling
```

#### Continuous Validation Strategy
```markdown
**Progressive Quality Validation**:
- **Issue Level**: Each issue passes quality gates before completion
- **Wave Level**: Each wave completion verified before next wave starts
- **Phase Level**: Each phase meets success criteria before progression
- **Epic Level**: Complete epic validation before final sign-off

**Quality Metrics Tracking**:
- Code coverage: Target 90%+ for core functionality
- Test pass rate: 100% for all automated tests  
- Performance metrics: All response time targets met
- Security validation: Zero critical vulnerabilities
- Documentation coverage: 100% API endpoint documentation
```

### Step 5: Risk Mitigation Pre-Planning

#### Technical Risk Mitigation
```markdown
**Common Technical Risks** (With pre-planned mitigation):

**External Dependency Risks**:
- **Risk**: Third-party API downtime or rate limiting
- **Mitigation**: Fallback mechanisms, local caching, graceful degradation
- **Validation**: Integration testing with simulated failures

**Performance Risks**:
- **Risk**: Response times exceed targets under load
- **Mitigation**: Performance testing throughout development, optimization strategies
- **Validation**: Load testing at each major milestone

**Security Risks**:
- **Risk**: Authentication vulnerabilities or data exposure
- **Mitigation**: Security review at each phase, automated vulnerability scanning
- **Validation**: Penetration testing and security audit

**Integration Risks**:
- **Risk**: Component integration failures or data inconsistencies
- **Mitigation**: Contract-driven development, comprehensive integration testing
- **Validation**: End-to-end workflow testing
```

#### Coordination Risk Mitigation
```markdown
**Coordination Risk Management**:

**Agent Coordination Risks**:
- **Risk**: Work conflicts or duplicate effort
- **Mitigation**: Clear work stream separation, regular coordination checkpoints
- **Validation**: Daily progress synchronization, conflict detection systems

**Dependency Management Risks**:
- **Risk**: Blocking dependencies or circular dependency issues
- **Mitigation**: Dependency graph monitoring, alternative path planning
- **Validation**: Daily dependency satisfaction checks

**Quality Consistency Risks**:
- **Risk**: Inconsistent implementation approaches across parallel streams
- **Mitigation**: Shared standards, cross-stream code review, architectural guidelines
- **Validation**: Code quality metrics and consistency checks
```

### Step 6: Success Criteria Pre-Definition

#### Execution Success Metrics
```markdown
**Development Velocity Metrics** (Targets for 11x improvement):
- **Epic Completion Time**: 2 weeks (vs. 20-week traditional approach)
- **Issue Resolution Rate**: 4-6 issues per week per agent
- **Parallel Efficiency**: 4-5x through coordinated streams
- **Rework Rate**: <5% of issues require significant rework
- **Quality Gate Pass Rate**: >95% first-time pass rate

**Quality Achievement Metrics**:
- **Specification Alignment**: 95%+ implementation matches specification
- **Test Coverage**: 90%+ automated test coverage achieved
- **Performance Targets**: All response time requirements met
- **Security Standards**: Zero critical vulnerabilities, all standards met
- **Documentation Completeness**: 100% API and operational documentation

**Collaboration Efficiency Metrics**:
- **Coordination Overhead**: <10% of total development time
- **Conflict Resolution**: Zero merge conflicts requiring manual resolution
- **Knowledge Transfer**: 100% cross-team knowledge sharing for critical components
- **Stakeholder Satisfaction**: >90% satisfaction with delivery quality and timing
```

## Pre-Execution Checklist

### Epic Optimization Validation
```markdown
**Pre-Execution Certification** (All items required):
- [ ] Epic complexity score >85 (implementation ready)
- [ ] All issues properly sized and scoped (no XL issues)
- [ ] Parallel execution streams clearly defined and conflict-free
- [ ] Agent assignments optimized for capabilities and workload
- [ ] Quality gates configured and automation tested
- [ ] Risk mitigation strategies defined and resources allocated
- [ ] Success criteria measurable and achievable
- [ ] Coordination procedures documented and communicated
- [ ] Fallback plans prepared for identified risks
- [ ] Resource allocation confirmed and team capacity verified

**Optimization Quality Score**: ___/100 (Target: 90+ for optimal execution)
```

### Execution Readiness Report Template
```markdown
# Epic [ID] Pre-Execution Optimization Report

## Optimization Summary
- **Parallel Execution Streams**: X streams identified
- **Agent Assignment Efficiency**: X% optimal assignment achieved
- **Risk Mitigation Coverage**: X critical risks addressed
- **Quality Gate Coverage**: X% automated validation configured

## Execution Plan Overview
- **Wave 1**: [X parallel streams, Y issues, Z days]
- **Wave 2**: [X parallel streams, Y issues, Z days]
- **Coordination Points**: [X critical handoffs identified]
- **Quality Checkpoints**: [X validation gates configured]

## Resource Allocation
- **phase-implementer**: [X issues, Y estimated hours]
- **precommit-compliance-reviewer**: [X review streams, Y coordination points]
- **Additional specialists**: [As needed for infrastructure, integration]

## Risk Management
- **Technical Risks**: [X identified, Y mitigated]
- **Coordination Risks**: [X identified, Y mitigated]
- **Quality Risks**: [X identified, Y mitigated]

## Success Predictions
- **Estimated Completion**: [X days vs Y traditional approach]
- **Quality Score Prediction**: [X/100 based on preparation quality]
- **Efficiency Multiplier**: [Xx improvement over traditional development]

## Go/No-Go Recommendation
☑ **GO**: Epic optimized and ready for high-velocity execution
☐ **NO-GO**: Additional optimization required (specify requirements)
```

This pre-optimization framework ensures epics are configured for maximum execution efficiency while maintaining the proven 95%+ quality standards and 11x velocity improvements.
