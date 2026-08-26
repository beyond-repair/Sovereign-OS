# Layer 0 — Human Kernel

**Purpose**: Maintain operator sovereignty.

## Responsibilities

- Human state monitoring (cognitive load, fatigue, alignment)
- Goal hierarchy management
- Override authority (never revocable)
- Recovery protocols
- Reflection and diagnostics

## Outputs

Intent, Priorities, Constraints, Authority grants.

## Key Interfaces

- `GET /human/state`
- `POST /human/override` (authenticated, logged)
- Hardware emergency stop support (GPIO / biometric)

## Invariants

INV-001 (root access never revoked), INV-009 (human uptime co-equal).

## Tech Notes

- FastAPI or Rust backend
- Neo4j or SQLite for goals
- InfluxDB / time-series for state
- Optional Raspberry Pi + biometric for physical override
