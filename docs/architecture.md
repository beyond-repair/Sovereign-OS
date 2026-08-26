# SovereignOS Architecture Overview

## Layers

**Layer 0 — Human Kernel**  
Operator sovereignty, state monitoring, goals, overrides, recovery.  
Invariant: Human root access can never be revoked (INV-001).

**Layer 1 — Constitutional Control Plane**  
Authority verification, evidence validation, risk assessment, refusal, audit, rollback.  
Invariant: No action bypasses the control plane.

**Layer 2 — Meta-Governance**  
Policy evolution, threshold calibration, model upgrade & schema migration approval, constitutional review.  
Invariant: No subsystem may modify governance rules directly (INV-011, INV-012).

**Layer 3 — Strategic Brains**  
Executive, Operations, Financial, Intelligence, Governance brains.  
Produce plans and recommendations only. Cannot execute.

**Layer 4 — Knowledge Infrastructure**  
Personal KG, Company KG, Capital KG, Evidence Repository.  
Domains isolated unless explicitly authorized (INV-006).

**Layer 5 — Agent Runtime**  
Sandboxed agents, tools, connectors, budget & time limits, circuit breakers.  
Agents possess no standing authority; authority is delegated per task (INV-010).

**Capital Kernel** (cross-cutting)  
Cash runway, burn, liquidity, risk concentration. Enforces INV-008.

## Data Flow

Human Intent → Human Kernel → Control Plane (gates) → Strategic Brains (plans) → Control Plane (re-validate) → Agent Runtime (execute under constraints) → Knowledge + Audit + Capital health update.

All paths return through the Control Plane for logging.
