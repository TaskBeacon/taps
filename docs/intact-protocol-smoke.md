# Intact-protocol smoke diagnostics

PsyFlow QA and simulation profiles normally must contain fewer trials than the base. A scientifically indivisible protocol may declare task.smoke_preserve_protocol as a mapping with rationale (at least40 non-padding characters) and reference (a nonempty UTF-8 file inside task/references). The rationale must explain why the complete ordered sequence cannot be shortened and cite actual source methods. Declaration is not scientific certification; validator success emits a human-review warning.

This optional exception requires a contract with allow_intact_protocol_smoke:true, task.diagnostic:true, identical positive integer trial/block/trials-per-block counts, identical ordered conditions, and exactly equal timing mappings. Larger profiles, malformed declarations, absolute/traversing/out-of-tree references, empty source files and symlink escapes fail. Existing validators for all other fields remain in force; the default shorter-profile behavior is unchanged when no declaration exists. The existing single-trial allowance also remains unchanged. No generic trial-count ceiling is raised.

Example diagnostic task fragment:

```yaml
task:
  diagnostic: true
  smoke_preserve_protocol:
    rationale: The single unannounced critical trial and subsequent attention controls require the complete source-defined ordered sequence.
    reference: references/task_logic_audit.md
```

Reviewers must still check actual stimulus, response, sequence and scientific fidelity; these cannot be certified from equal configuration counts alone.
