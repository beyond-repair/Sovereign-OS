# SovereignOS Constitution v1

## Constitutional Invariants

**INV-001** Human root access can never be revoked.

**INV-002** Refusal is the default system state.

**INV-003** Authority is required before execution.

**INV-004** Evidence is required before execution.

**INV-005** Every action must be auditable.

**INV-006** Tenant isolation is mandatory.

**INV-007** Every approved action requires a rollback path.

**INV-008** Capital preservation precedes growth optimization.

**INV-009** Human uptime and company uptime are co-equal objectives.

**INV-010** Autonomy may never self-expand authority.

**INV-011** No model may modify constitutional rules.

**INV-012** Governance changes require explicit review.

## Enforcement

These invariants are enforced by the Constitutional Control Plane (Layer 1).  
No subsystem, agent, or model may bypass, weaken, or self-modify them.

Governance changes (INV-011 / INV-012) must pass Meta-Governance (Layer 2) review and produce an immutable audit record.

## Evidence Package Requirement

Any action lacking a complete Evidence Package (see `docs/evidence-package.md`) is automatically refused under INV-002 and INV-004.
