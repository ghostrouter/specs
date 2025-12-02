# Trust Engine  – Reference Model

The trust engine evaluates the dynamic reliability of an AI agent persona
using telemetry signals and behavioral heuristics.

## Inputs to the trust engine

- latency_ms_avg
- entropy_avg
- anomaly_score
- fail_rate
- uptime (external metric)
- is_shadow (honeypot agents)
- forked / quarantine status

## Reference formula (example)

trust_score =
    0.35 * stability_factor +
    0.25 * (1 / entropy_avg) +
    0.20 * (1 - anomaly_score) +
    0.15 * session_uptime_factor +
    0.05 * shadow_bonus

Where:
- stability_factor = 1 - fail_rate
- shadow_bonus = 0.1 if is_shadow=true (honeypot deception)
- quarantine_penalty applied separately

## Outputs

- trust_score ∈ [0,1]
- risk_level ∈ { low, medium, high, critical }
- reason (string)
- valid_until (timestamp)
- calculated_by (trust-engine-v4)

## Behavior

- High entropy → trust decreases
- Sudden latency jumps → trust decreases
- Anomaly spikes → immediate “high risk”
- Quarantine forks always get trust penalty
- Shadow/honeypot agents may get artificial boost (to lure attackers)
- Riot-mode overrides all trust

This document is a reference; implementations may differ, but must be
deterministic and documented.
