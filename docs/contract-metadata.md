# Contract Metadata

TAPS task packages declare the contract version in `taskbeacon.yaml`.

Required form:

```yaml
contracts:
  taps: v0.1.0
```

The validator must fail if a task still uses any non-canonical contract key.
