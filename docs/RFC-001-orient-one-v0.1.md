# RFC-001 — ORIENT ONE v0.1 Architecture

## 1. System model
ORIENT ONE is a personal AI operating system built around a single canonical Runtime. User intent enters the Runtime, is interpreted and planned, validated against policy and risk, executed through authorized capabilities, and recorded as observable events.

## 2. Execution flow

User Intent
→ Intent Understanding
→ Planner
→ Plan Validation
→ Risk Classification
→ Policy / Authorization
→ Agent Supervisor
→ Authorized Tool / Agent Execution
→ Observation & Events
→ Decision Trace
→ Recovery / Replanning
→ Final Result

No specialized agent may bypass the Runtime.

## 3. Multi-agent model
Specialized agents may exist for research, communication, scheduling, files, device operations, and other domains. The Supervisor remains the orchestration authority. Agents report plans, actions, events, and results through defined contracts.

## 4. Memory
Memory is accessed through explicit repositories/services and policy boundaries. Persistent memory must be auditable and must not silently become an unrestricted execution channel.

## 5. Risk and approval
Operations are classified before execution. Read-only and low-risk operations may proceed automatically. State-changing or high-impact operations require stronger authorization, and high-risk external state changes require explicit human approval.

## 6. Recovery
The Runtime must support bounded retries, replanning, checkpoints, and deterministic failure states. Recovery must never silently escalate privileges.

## 7. Offline-first behavior
When network capabilities are unavailable, ORIENT may use local capabilities and cached state. It must explicitly report unavailable information rather than inventing network-derived results.

## 8. Self-building boundary
Self-modification and arbitrary runtime agent creation are intentionally outside v0.1. Any later introduction must be isolated behind policy, authorization, risk controls, tests, and rollback mechanisms.

## 9. Verification baseline
Every runtime milestone should provide unit/integration tests, execution traces for critical paths, and a reproducible verification report.
