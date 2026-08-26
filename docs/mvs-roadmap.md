# Minimum Viable Sovereign (MVS) Roadmap

| Phase | Layer / Focus            | Deliverables                                              | Recommended Stack                  |
|-------|--------------------------|-----------------------------------------------------------|------------------------------------|
| 1     | Control Plane            | Authority Engine, Evidence Engine, Refusal Engine, Audit  | OPA, FastAPI/Go, SQLite/event store|
| 2     | Human Kernel             | Goals, Priorities, Uptime metrics, Override controls      | Neo4j, InfluxDB, FastAPI           |
| 3     | Knowledge Infrastructure | Neo4j graphs, Evidence Repository, Provenance             | Neo4j, IPFS or content-addressed   |
| 4     | Agent Runtime            | Sandboxed agents, tools, budget & circuit breakers        | Docker/K8s, NATS, Redis            |
| 5     | Meta-Governance          | Policy management, threshold calibration, review workflows| DVC/Git, Casbin, formal methods    |

**Start with Phase 1.** It is the foundation that all other layers depend on.

Testing requirement: Chaos engineering (random container kills, authority injection attempts) to validate INV-007 and INV-002.
