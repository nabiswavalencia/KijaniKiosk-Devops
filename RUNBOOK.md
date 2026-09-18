# Deployment Failure Runbook

This document outlines the standard recovery procedure to follow when a deployment fails in production. Following these steps consistently turns incidents into learning opportunities rather than repeated fire-fighting.

## Recovery Steps

1. **Halt further deployments**
   Freeze the pipeline immediately so no additional changes are introduced while the issue is being investigated.

2. **Assess the failure**
   Check CI/CD logs and recent commits (`git log --graph --oneline`) to identify what changed and likely caused the failure.

3. **Roll back to the last known-good release**
   Redeploy the most recent stable tagged version (e.g. `v0.1`) to restore service quickly.Example: `git checkout v0.1`
cat > RUNBOOK.md << 'EOF'
# Deployment Failure Runbook

This document outlines the standard recovery procedure to follow when a deployment fails in production. Following these steps consistently turns incidents into learning opportunities rather than repeated fire-fighting.

## Recovery Steps

1. **Halt further deployments**
   Freeze the pipeline immediately so no additional changes are introduced while the issue is being investigated.

2. **Assess the failure**
   Check CI/CD logs and recent commits (`git log --graph --oneline`) to identify what changed and likely caused the failure.

3. **Roll back to the last known-good release**
   Redeploy the most recent stable tagged version (e.g. `v0.1`) to restore service quickly.Example: `git checkout v0.1`

4. **Verify recovery**
   Confirm the rollback restores expected behavior — run health checks, smoke tests, and confirm the application is serving traffic normally.

5. **Communicate status**
   Notify the team and any affected stakeholders that the incident is mitigated and service is restored.

6. **Document the incident**
   Record the root cause, timeline, impact, and resolution steps. Update this runbook if the process revealed a gap or missing step.

## Notes
- Never skip the rollback verification step, even under time pressure.
- Every incident should result in at least one improvement to prevent recurrence (a test, an alert, or a process change).
