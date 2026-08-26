# Layer 1 — Constitutional Control Plane

**Purpose**: Govern every system action.

## Core Components

| Component          | Description                          | Implementation Notes                  |
|--------------------|--------------------------------------|---------------------------------------|
| Authority Engine   | Validates permission                 | OPA / Policy-as-Code                  |
| Evidence Engine    | Validates Evidence Package           | Pydantic schema + confidence scoring  |
| Risk Assessor      | Severity / likelihood / impact       | Thresholds + optional Monte Carlo     |
| Refusal Engine     | Defaults to reject                   | State machine, escalate on boundary   |
| Audit Log          | Immutable record                     | Append-only + cryptographic hash chain|

## Interfaces

- `POST /control/validate` — submit action for approval
- `GET /control/audit/{action_id}` — retrieve audit record
- Webhooks for escalation (Slack / Telegram / Human Kernel)

## Invariants Enforced

INV-002, INV-003, INV-004, INV-005, INV-007, INV-010

## Tech Stack Recommendation

- Backend: Go or FastAPI (Python)
- Policy: Open Policy Agent (OPA)
- Audit store: SQLite / Postgres with hash chaining or event store
- Cache: Redis

## MVS Phase 1 Deliverable

Fully functional Authority + Evidence + Refusal engines + immutable Audit Log.
