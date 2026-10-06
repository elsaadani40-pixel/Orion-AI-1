# ORIENT ONE — ENGINEERING CONSTITUTION

## Mission
ORIENT ONE is an autonomous personal AI agent / personal operating system. It must become a real, reliable system—not a demo, toy, temporary prototype, or superficial showcase.

## Core architecture
- One canonical Runtime owns execution.
- Agent Supervisor coordinates specialized agents.
- Model Router selects models according to task, policy, cost, and availability.
- Tools and Memory are capability-controlled services.
- Policy and Authorization govern every capability boundary.
- Risk Classification determines whether an operation is allowed, simulated, or requires human approval.
- High-risk external state changes require explicit human approval.
- Events, Decision Trace, Recovery, and Observability are first-class runtime concerns.

## Security boundaries
- Agents do not bypass the Runtime.
- Agents do not directly mutate protected state.
- Early ORIENT stages must not self-modify the Runtime.
- Early ORIENT stages must not create and execute arbitrary new agents inside the Runtime.
- Self-building/self-modifying behavior is a later, separately governed capability.
- Offline mode must never fabricate unavailable network results.

## Engineering rules
1. TypeScript is the primary language.
2. Prefer open-source and local-first components.
3. Avoid paid/proprietary dependencies where a viable free/open alternative exists.
4. No demo-only architecture.
5. Every meaningful capability needs tests and observable failure behavior.
6. Keep the canonical execution path explicit and auditable.
7. Changes to runtime contracts require architectural review.

## Repository policy
GitHub is the canonical source-control home for ORIENT ONE. Never commit secrets, local credentials, generated caches, or private user data.

## Current bootstrap
The repository is being initialized before the complete canonical source tree is pushed. Do not mistake repository bootstrap files for implementation completion.
