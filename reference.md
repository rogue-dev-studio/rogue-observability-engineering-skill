# Observability Engineering - Reference

## Logging

- Useful fields: timestamp, level, service, request_id, action, outcome
- Error: message + error class; stack traces only in non-production or protected sinks
- Do not log full bodies that contain credentials

## Health

| Endpoint | Meaning |
|----------|--------|
| Liveness | Process is alive |
| Readiness | Ready for traffic (DB reachable, migrations complete) |

## Metrics (minimal)

- Request rate, error rate, latency p95 for P0 endpoints
- Queue depth when using jobs

## Anti-patterns

- Unstructured `console.log` in production
- Health always returns 200 even when DB is down
- Metric label cardinality explosion (user id as a label)
