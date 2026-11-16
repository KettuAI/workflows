Use it to restructure code you depend on without changing what it does.

1. Plan describes the target shape and the behavior that must not change. You approve it.
2. Pin behavior adds tests for today's behavior before any code moves.
3. Refactor changes the code in small steps and may not touch a single test.
4. Review on another agent checks that behavior is unchanged and no test was weakened.

The work stays as commits on the task's branch; push and merge it when you are ready.
