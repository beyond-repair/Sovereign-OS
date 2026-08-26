# Layer 5 — Agent Runtime

**Purpose**: Execute approved work only.

Components: Specialized agents, sandboxed execution (Docker/K8s + seccomp/AppArmor/Firecracker), tool integrations, external connectors.

Controls: Scoped permissions, budget limits, circuit breakers, time limits.

Invariant: Agents possess no standing authority. Authority is delegated per task (INV-010). Every action has a rollback path (INV-007).

Tech: Docker + Kubernetes, NATS message bus, Redis for budgets/tokens, pre-task snapshots for rollback.
