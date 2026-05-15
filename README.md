# TAPS

TAPS (Task and Paradigm Structure) is the TaskBeacon task package standard.

This repository is the source of truth for:

- versioned contracts under `contracts/vX.Y.Z`
- task package metadata conventions
- task layout and artifact documentation
- minimal Python and web task examples

This repository does not provide validator tooling. Tooling lives in
`TaskBeacon/taps-utils`.

## Contract Metadata

Every task package must declare:

```yaml
contracts:
  taps: v0.2.0
runtime:
  profile: psyflow
```

No other contract key is valid for TAPS validation.

TAPS v0.2.0 adds runtime profiles while keeping one contract identity.
Initial profiles are `psyflow`, `web`, and `godot`.
