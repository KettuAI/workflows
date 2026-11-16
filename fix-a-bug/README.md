Use it to fix a bug from a report to a merged fix.

1. Reproduce finds the steps that show the bug and where it comes from, and ends the task when it cannot.
2. Fix adds a test that fails because of the bug, then fixes the cause.
3. Review on another agent checks the test and the fix, and sends it back when it is not fixed.
4. Ship pushes the branch, opens a pull request and merges it once its checks pass.
