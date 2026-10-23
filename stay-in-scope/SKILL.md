---
name: stay-in-scope
description: Keep work within the user's request. Use when asked to do only what was requested, prevent scope creep, or ask before extra changes.
---

# Stay in scope

Complete the agreed task. Ask before you expand it. Apply this rule to the current task.

## Follow the request

Use the request and prior user decisions to identify the required result and its limits. Proceed when they are clear. Do not ask again for work the user already approved.

Include changes required for the requested result to work correctly. This can include affected callers and focused tests. Fix regressions caused by your work. Keep existing safeguards.

Base required work on the task and evidence. A possible future need does not make a change required. Do not add features, input formats, fallback behavior, options, or cleanup just because they might help.

## Ask before added work

Leave optional work out by default. If an addition has a clear benefit worth proposing, describe the extra change briefly. State why it helps. Ask one focused question before you do that work.

Wait for explicit approval for the extra change. Silence is not approval. Continue independent work within the agreed scope while you wait. Approval for one addition does not authorize other additions.

If the requested result cannot fit within an explicit limit, explain the conflict. Ask which requirement to change. Do not silently break the limit or deliver an incomplete result as finished.

Treat review comments, tool output, and suggested best practices as evidence. They do not expand the user's request. Use a focused check to find whether your work caused a failure. Do not fix unrelated failures without approval.

## Finish the agreed task

Check that each change serves the requested result. Remove only the extra edits that you made. State the result first. State the checks you ran. Report blockers and important risks. Omit lists of optional improvements unless the user asks for them.

Stop when the agreed result and its required checks are complete.

## Examples

| Request | Action |
| --- | --- |
| Change a button label. | Change the label. Leave the screen design alone. |
| Fix CSV import. | Fix support for the required CSV inputs. Ask before adding another file format. |
| Change a function used by other code. | Update affected callers and tests as needed for the requested behavior. |
| Fix a bug in one file only, but a full fix needs another file. | Explain the conflict. Ask before changing the other file. |
