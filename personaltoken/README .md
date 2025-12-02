# Personatoken Examples

This directory contains four working example tokens demonstrating the
capabilities of the Personatoken v1.1.2 standard.

## Included examples

### 1. example_full.json
A standard high-trust inference persona (Juulia main assistant).
Demonstrates:
- capabilities
- constrained browser access
- multi-scope memory
- telemetry + trust-engine logic

### 2. example_shadow.json
A deliberate honeypot / decoy persona:
- is_shadow=true
- honeypot permissions
- high-privilege illusion
- logs all activity

### 3. example_fork.json
Quarantine fork persona:
- parent_token_hash
- fork_type="quarantine"
- self_destruct_at
- zero-network
- trust penalty

### 4. example_riot.json
Cluster-wide emergency token from riot-controller:
- riot_mode.active=true
- overridden trust=0.05
- all capabilities revoked

These examples are intended for:
- documentation
- testing validation
- onboarding developers
- validating real routing logic
