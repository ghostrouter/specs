# Personatoken Standard v1.1.2
Ghost Router – AI-Native Zero-Trust Identity Layer

This folder contains the complete specification for the Personatoken
framework. Personatoken defines dynamic, context-aware identities for AI agents.
It includes permissions, tools, constraints, telemetry, trust, delegation,
shadow/honeypot personas, quarantine forks, and riot-mode cluster lockdown.

## Files

- **personatoken-v1.1.2.schema.json** – Formal JSON Schema
- **examples/** – Valid example tokens
- **trust-engine-v4.md** – Reference trust-score logic

## Features in v1.1.2

### Identity
- persona_id, display_name, version, tags  
- shadow personas (honeypot / decoy)

### Permissions
- capability- & constraint-based tooling
- memory scopes: none / session / tenant / global_limited
- honeypot=true
- self-destruct_at (for quarantine forks)

### Token modes
- full
- light
- delegated
- shadow
- fork
- riot (emergency override)

### Fork / Quarantine
- parent_token_hash
- fork_type
- trust penalties

### Riot-mode
- override trust
- override permissions
- cluster defense

### Telemetry & Trust
- entropy, latency, anomalies, fail_rate
- trust_score, valid_until, calculated_by
- shadow trust boost
- fork trust penalty

---

This is the world’s first AI-native Zero-Trust Identity Standard.

Maintained by: **GhostRouter Lab – Gary & Juulia (2025)**
