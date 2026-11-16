Use it for a change that spans a frontend and a backend.

1. Split divides the work and agrees the interface between the two sides.
2. Frontend and Backend are built at the same time, each on its own branch.
3. Integration test runs both together and sends a problem back to the side it came from.
4. Code review on another agent approves the change or sends it back to Split.
5. Ship pushes the branch, opens a pull request and merges it once its checks pass.
