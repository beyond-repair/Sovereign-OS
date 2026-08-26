# Layer 2 — Meta-Governance

**Purpose**: Govern the governance system.

Responsibilities: Policy evolution, threshold calibration, model upgrade approval, schema migration approval, delegation management, constitutional review.

Invariant: No subsystem may modify governance rules directly. All changes require constitutional review (INV-011, INV-012).

Tech: Versioned policies (Git/DVC), multi-sig style approvals, Casbin or equivalent RBAC, optional formal verification (TLA+/Alloy) for critical rules.
