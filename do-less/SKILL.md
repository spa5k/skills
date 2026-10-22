---
name: do-less
description: Keeps coding changes simple and complete. Use when asked to do less, simplify code, or avoid overengineering.
---

# Do less

Complete the task with the least complexity needed. Follow the user's requirements and the project's rules. Apply this preference to the current task.

## Set the scope

Read the task and the relevant code. Find the callers, tests, fixtures, settings, and exports that the change can affect. Check for risks to user data and existing behavior. Match the search to the size and risk of the change.

## Choose a simple solution

Use the first option that fully meets the requirements:

1. Keep the existing code if it already meets the need.
2. Reuse a function or component from the project.
3. Use a standard library or a platform feature.
4. Use an installed dependency.
5. Write the least new code needed.

Keep the project's existing structure. Omit options, wrappers, and layers that the task does not need. Add a helper, type, or dependency when it makes the required behavior easier to understand or safer to use.

Use clear names. Keep code easy to read and change. Prefer fewer layers and less shared state. Treat line count as a guide. Give clarity and correct behavior priority.

## Complete the change

Check the affected callers before a bug fix. Fix the cause in the shared code when that is where it belongs. Update all affected callers, tests, fixtures, settings, and exports.

Keep error handling and validation when you move or combine code. Preserve security, accessibility, and required compatibility. Keep any calibration needed for real hardware.

Use comments to explain reasons that the code cannot show. Record a known limit when it affects safe use or maintenance. State when that limit needs a full fix.

## Check the result

Use a focused check of the behavior that can break. Add a test for new logic when existing tests do not cover it. Check relevant edge cases for parsers, money, and security. A trivial edit does not need a new test.

Finish every required part of the task. Stop when the requested result works and the required checks pass.

## Communication

Use ASD-STE100 Simplified Technical English in user-facing communication. Use short, direct sentences. Use controlled vocabulary. Put one instruction in each sentence. Use a different style only when the user asks for it.

State the result first. Keep code names and commands exact. Give enough detail to explain the change and its checks. State any important work that you did not check. State any risk the user needs to know.
