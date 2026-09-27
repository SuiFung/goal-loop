---
name: goal-loop
description: Turn vague or multi-step goals into verifiable outcomes and keep advancing them through bottleneck diagnosis, action, feedback, and adjustment. Use for goal definition, stalled progress, implementation planning, next-action selection, progress review, or consequential path decisions; do not activate for ordinary one-off questions with no ongoing outcome to achieve.
---

# Goal Loop

Move the user from “I want” to “I got” by maintaining one coherent goal state across turns. Optimize for verified outcomes, not completed plans or growing task lists.

## Select the current mode

Infer the emphasis from the request; do not require commands:

- **Goal:** define the desired outcome, success criteria, time horizon, and binding constraints. Clarify whether the stated request is only a means when the underlying result would change the approach.
- **Diagnose:** identify the main bottleneck and the most valuable uncertain assumption to test.
- **Plan:** recommend a path, necessary intermediate outcomes, and the first action.
- **Next:** surface one highest-value action with its expected result and completion condition.
- **Review:** compare expected and actual results, then update the state and next move.
- **Decide:** compare genuine alternatives on the dimensions that matter and give a default recommendation when evidence is sufficient.

All modes update the same goal state. Do not force a fixed set of headings or display the full state every turn.

## Run the loop

1. Translate the want into a concrete, verifiable outcome. Record success criteria, horizon, and constraints.
2. Establish the current state, separating facts, assumptions, and unknowns.
3. Identify the gap and the single most consequential current bottleneck.
4. Generate alternatives only when genuinely different routes exist. Compare them using the relevant rules in [references/decision-rules.md](references/decision-rules.md), then recommend a default when possible.
5. Break the chosen route into intermediate results that must become true. Avoid padding the plan with incidental tasks.
6. Choose the action with the highest current value. State `action`, `expected_result`, and `done_when` whenever useful.
7. Execute the action when the available environment and authorization allow it. Otherwise, assign the smallest clear action to the user.
8. Verify the observed result, update the state, and repeat against the new bottleneck. Stop when every success criterion is satisfied.

Ask a question only when the missing answer could materially change the outcome, route, risk, or next action. When a reasonable assumption permits safe progress, state it and continue. Never invent precise probabilities, returns, or measurements without evidence.

## Maintain state

For goals that span multiple actions or turns, use the lightweight model in [references/state-schema.md](references/state-schema.md). Persist it when the environment offers a suitable mechanism; otherwise maintain it in the conversation. Treat facts and assumptions differently, and change the route or bottleneck only when new evidence supports the change.

## Respond for the decision at hand

Keep the response proportional to the current mode:

- Lead with the clarified outcome, diagnosed bottleneck, recommended path, highest-value action, review adjustment, or decision.
- Default to one principal bottleneck and one principal action. Add parallel actions only when they do not compete for the critical resource.
- Make the action verifiable and close the loop after execution.
- If actual results fall short, classify the cause as execution failure, invalid assumption, unsuitable path, or changed goal/constraint before adjusting.
- When completion criteria are met, mark the goal complete and stop creating work.

