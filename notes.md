# The Three Ways of DevOps

## First Way: Flow
Focuses on the fast, left-to-right movement of work from Development to Operations to the customer. Key practices include:
- Making work visible (e.g. the Commit → Build → Test → Package → Deploy pipeline)
- Reducing batch sizes so changes are smaller and easier to release
- Eliminating handoff delays and unnecessary approvals between teams
- Automating repetitive steps (builds, tests, deployments) to remove bottlenecks

## Second Way: Feedback
Focuses on creating fast, constant feedback loops from right to left, so problems are caught close to where they're introduced. Key practices include:
- Automated testing and CI pipelines that fail fast on bad commits
- Monitoring and alerting in production to surface issues early
- Shortening the time between a change being made and its effects being known
- Treating operations signals (logs, metrics, incidents) as input back into development

## Third Way: Continual Learning and Experimentation
Focuses on building a culture of high trust and continuous improvement. Key practices include:
- Treating failures/incidents as learning opportunities, not blame targets
- Capturing operational knowledge as reusable documentation (e.g. runbooks)
- Encouraging experimentation and risk-taking within safe boundaries
- Repeating practice and drilling so improvements become habitual
