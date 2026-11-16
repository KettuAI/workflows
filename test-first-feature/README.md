Use it when the behavior can be written down precisely and you want proof the code does exactly that.

1. Spec writes the behavior as examples. You approve it.
2. Tests turns each example into a test and checks it fails for the right reason.
3. Build writes the code until the tests pass and may not change them.
4. Code review on another agent checks the code against the spec and sends work back to the build or the tests.
