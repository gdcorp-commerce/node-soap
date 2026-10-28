## Jira Ticket
<!-- Link to Jira ticket (required) -->
[COMMERCE-XXXX](https://godaddy-corp.atlassian.net/browse/COMMERCE-XXXX)

## Type of Change
<!-- Check all that apply -->
- [ ] Bug fix (non-breaking change fixing an issue)
- [ ] New feature (non-breaking change adding functionality)
- [ ] Breaking change (fix or feature causing existing functionality to change)
- [ ] Configuration change
- [ ] Infrastructure/deployment change
- [ ] Documentation update
- [ ] Dependency update

## Summary
<!-- Provide a clear, concise summary of what this PR accomplishes -->

**What changed:**
<!-- Describe the technical changes made -->

**Why:**
<!-- Explain the business/technical reason for this change -->

**Impact:**
<!-- Who/what is affected by this change? -->

## Testing
<!-- Required: Provide evidence that this change works as expected -->

### Automated Tests
- [ ] Unit tests added/updated
- [ ] Integration tests added/updated
- [ ] E2E tests added/updated
- [ ] All tests passing

**Test coverage:** <!-- e.g., "Added 5 unit tests covering new validation logic" -->

### Manual Testing
<!-- Describe manual testing performed -->
**Test environment:** <!-- e.g., dev, test, ote -->
**Steps performed:**
1. 
2. 
3. 

**Results:** <!-- What happened? Include screenshots/logs if relevant -->

### Visual Evidence
<!-- For UI changes: Include screenshots/recordings showing before & after -->
<!-- For API changes: Include example requests/responses -->
<!-- For bug fixes: Show the bug is resolved -->

<details>
<summary>Screenshots/Evidence</summary>

<!-- Paste screenshots, GIFs, or terminal output here -->

</details>

## Feature Flags
<!-- If this change is behind a feature flag, provide details -->
- [ ] N/A - No feature flag needed
- [ ] Feature flag: `flag_name`
  - Dev: [link]
  - Test: [link]
  - OTE: [link]
  - Prod: [link]
- [ ] Rollout plan documented


### Database Changes
- [ ] N/A - No database changes
- [ ] Schema migration included
- [ ] Migration tested in non-prod
- [ ] Rollback plan documented

### Dependencies
- [ ] N/A - No dependency changes
- [ ] Dependencies added/updated (reviewed for security/licensing)
- [ ] Breaking dependency changes documented

### Deployment Order
- [ ] N/A - Standard deployment
- [ ] Specific deployment order required (document below)

<!-- If special deployment order/steps needed, document here -->

## Observability
<!-- How will this change be monitored? -->

### Logging
- [ ] N/A - No new logging
- [ ] Appropriate log levels used
- [ ] No sensitive data in logs
- [ ] Structured logging format followed

### Metrics/Monitoring
- [ ] N/A - No new metrics
- [ ] Metrics/dashboards added
- [ ] Alerts configured
- [ ] Links to monitoring: <!-- dashboard URLs -->

## Documentation
<!-- Keep documentation up to date -->
- [ ] README updated
- [ ] API documentation updated
- [ ] Architecture/design docs updated
- [ ] Runbook/operational docs updated
- [ ] Confluence pages updated: <!-- link if applicable -->
- [ ] OpenAPI/Swagger specs updated

## Quality Checklist
<!-- Ensure code quality standards -->
- [ ] Code follows team style guidelines
- [ ] Backward compatibility maintained (or breaking changes documented)
- [ ] Performance impact considered
- [ ] Accessibility standards met (for UI changes)

## Rollback Plan
<!-- How to rollback if issues arise in production -->
- [ ] Simple revert of this PR is sufficient
- [ ] Requires manual steps (document below)
- [ ] Feature flag can disable this feature

<!-- Document rollback steps if not a simple revert -->

## Related PRs
<!-- Link any related PRs in this or other repos -->
- 

## Reviewer Notes
<!-- Specific areas where you want reviewer feedback -->
<!-- Any context that will help reviewers? -->

---

**Delete any sections that don't apply to your change** to keep the PR focused and readable.
