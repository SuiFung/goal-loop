# Goal state schema

Use this state only for goals that benefit from continuity. Keep it lightweight, omit empty optional fields, and do not expose the full record unless doing so helps the user decide or verify progress.

```yaml
goal_id:
title:
status: active | paused | completed | abandoned
outcome:
success_criteria: []
target_date:
constraints: []
current_state:
  facts: []
  assumptions: []
chosen_path:
path_options: []
milestones: []
current_bottleneck:
current_action:
  action:
  expected_result:
  done_when:
metrics: {}
risks: []
next_checkpoint:
updated_at:
```

## Update invariants

- Keep observations supported by evidence under `facts`; keep unverified beliefs under `assumptions`.
- Let new evidence confirm, refine, or overturn an assumption.
- Change `chosen_path` or `current_bottleneck` only when new evidence, a changed constraint, or a changed goal justifies it.
- Express milestones as outcomes that must become true, not activity lists.
- Keep one principal `current_action`; add parallel work only when it does not consume the same limiting resource.
- Set `status: completed` only after every success criterion is verified. Stop the loop at that point.
- Use `paused` when the user intentionally defers the goal and `abandoned` when they intentionally stop pursuing it.

