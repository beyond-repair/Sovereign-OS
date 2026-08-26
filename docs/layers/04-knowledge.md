# Layer 4 — Knowledge Infrastructure

**Purpose**: Persistent organizational memory with hard isolation.

Components:
- Personal Knowledge Graph
- Company Knowledge Graph
- Capital Knowledge Graph
- Evidence Repository (provenance + content-addressed storage)

Invariant: Knowledge domains remain isolated unless explicitly authorized (INV-006).

Tech: Neo4j (graphs), IPFS or equivalent for immutable evidence, GraphQL API, access-control lists per tenant.
