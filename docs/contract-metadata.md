# Contract Metadata

TAPS task packages declare the contract version in `taskbeacon.yaml`.

Required form:

```yaml
contracts:
  taps: v0.2.0
runtime:
  profile: web
```

The validator must fail if a task still uses any non-canonical contract key.

`runtime.profile` selects the runtime-specific contract checks. Current profiles:

- `psyflow`: Python/PsychoPy tasks using `main.py` and `src/run_trial.py`.
- `web`: TypeScript browser tasks using `main.ts` and `src/run_trial.ts`.
- `godot`: minimal extension point for future Godot tasks.
