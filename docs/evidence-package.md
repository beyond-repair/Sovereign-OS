# Evidence Package Standard

Every action proposal submitted to the Control Plane must contain a complete Evidence Package. Incomplete packages are refused by default (INV-002, INV-004).

```json
{
  "action_id": "uuid",
  "timestamp": "ISO8601",
  "requestor": "human|agent|system",
  "authority": {
    "source": "human|role|policy",
    "scope": ["read", "write", "execute"],
    "expiration": "ISO8601"
  },
  "evidence": {
    "confidence": 0.0-1.0,
    "supporting_sources": ["uuid or uri"],
    "verified": true
  },
  "risk": {
    "severity": "low|medium|high",
    "likelihood": 0.0-1.0,
    "impact": "reversible|irreversible"
  },
  "expected_value": {
    "roi": "float or null",
    "strategic_alignment": 0.0-1.0
  },
  "rollback": {
    "available": true,
    "rollback_procedure": "string description or reference"
  },
  "decision": {
    "status": "approved|rejected|escalated|require_evidence|require_human_review",
    "reviewer": "human_id|null"
  }
}
```

## Validation Rules

- All required fields must be present and type-correct.
- `authority.expiration` must be in the future at evaluation time.
- `evidence.confidence` < configured threshold → escalate or refuse.
- `rollback.available` must be `true` for any irreversible impact (INV-007).
- Capital-related actions must also satisfy Capital Kernel health checks (INV-008).
