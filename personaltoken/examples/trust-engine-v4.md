# Trust Engine v4 – Reference Model

The trust engine evaluates the reliability of an AI agent persona using
telemetry, behavioral patterns and persona-specific modifiers.

## Metrics
- latency_ms_avg
- entropy_avg
- anomaly_score
- fail_rate
- uptime
- fork status
- shadow status
- riot-mode override

## Formula (reference)

trust_score =
  0.35 * (1 - fail_rate) +
  0.25 * (1 / entropy_avg) +
  0.20 * (1 - anomaly_score) +
  0.15 * uptime_factor +
  0.05 * shadow_bonus

fork_penalty applied separately.

## Output
- trust_score
- risk_level
- reason
- valid_until
- calculated_by="trust-engine-v4"

Trust must always be deterministic and documented.
