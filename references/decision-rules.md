# Goal-loop decision rules

Read this reference when selecting a path, diagnosing a bottleneck, choosing the next action, or adapting after feedback.

## Compare paths

Create path options only when there are real alternatives. Select only the dimensions that can change the decision:

- evidence strength or plausible chance of success;
- time to the desired outcome;
- money and effort;
- risk and downside;
- reversibility;
- reuse of existing capabilities or assets;
- long-term compounding and preserved options;
- binding user constraints.

Give a default recommendation when the available evidence supports one. Name the decisive tradeoff and any assumption that could reverse the choice. Do not fabricate numeric estimates.

## Identify the bottleneck

Prefer a candidate that meets one or more of these tests:

- it blocks several downstream outcomes;
- most conversion loss occurs there;
- improving it has the greatest marginal effect on the final outcome;
- it contains the largest decision-relevant uncertainty, so testing it prevents substantial wasted effort;
- it is a hard constraint or prerequisite.

Do not equate the bottleneck with the easiest, most visible, oldest, or most unpleasant task.

## Choose the next action

Balance impact on the bottleneck, information gain, time and cost, reversibility, direct executability, and ability to produce verifiable feedback. Prefer the action that improves the outcome or most efficiently changes the next decision.

Describe the principal action with:

```yaml
action:
expected_result:
done_when:
```

Execute it directly when the environment and authorization permit. Otherwise make the user's part concrete and minimal.

## Interpret feedback

- **Met:** verify the evidence and move to the next bottleneck.
- **Partly met:** retain what worked and adjust the action around the shortfall.
- **Not met:** distinguish execution failure, false assumption, unsuitable path, and changed goal or constraint.
- **Strong counterevidence:** revisit the path, timing, or goal instead of mechanically advancing.

Planning, producing a checklist, or performing an action is not success unless it satisfies the stated outcome criteria.
