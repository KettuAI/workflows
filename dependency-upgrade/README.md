Use it to bring a project's dependencies up to date without surprises.

1. Survey lists what is outdated, the breaking changes that affect this project and an order to upgrade in. You approve it.
2. Upgrade goes group by group, fixing breaking changes at their cause, with one commit per group.
3. Verify on another agent installs from scratch, runs everything and looks for silenced errors.
4. Ship opens a pull request and waits for its checks. It does not merge.

Name the dependencies in the requirement to limit the upgrade to them.
