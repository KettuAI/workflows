Use it when something is slow or heavy and you want it fixed with proof, not guesses.

1. Baseline builds a repeatable measurement and records where you start.
2. Profile finds what is actually expensive with a profiler.
3. Optimize fixes the top bottleneck.
4. Measure again repeats the same measurement. No real gain sends the work back to profiling.
5. Code review on another agent checks the faster code is still correct.

Say in the requirement what is slow and, if you have one, the target.
