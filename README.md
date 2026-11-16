# Kettu workflows

Workflows for [Kettu](https://github.com/KettuAI/Kettu)'s tasks. A workflow is a flowchart of steps that agents carry out one after another, each in its own session, with your review where it matters. Kettu enforces the steps and the arrows between them; who does each step is picked when it starts, unless you pin one.

These are published to the Kettu Marketplace by `kettu-labs`. In Kettu, open Marketplace › Workflows and add one from Community, or paste the GitHub address of a `workflow.yaml` under Added from GitHub. Every workflow waits for your approval before it can start a task, and again after each update.

| Workflow                                                           | What it does                                                                                                                                                     |
| ------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Compare two approaches](compare-approaches/workflow.yaml)         | Define the question and how to judge the answer, build two quick prototypes at once in separate branches, then compare them with evidence for your decision.     |
| [Dependency upgrade](dependency-upgrade/workflow.yaml)             | Survey outdated dependencies and their breaking changes, upgrade them in the order you approve, verify the build and tests, then open a pull request.            |
| [Feature development](feature-development/workflow.yaml)           | Research whether it is worth doing, design and plan it with your review, build it, review the code on another agent, then ship it.                               |
| [Fix a bug](fix-a-bug/workflow.yaml)                               | Reproduce the bug, fix it with a test, review the fix on another agent, then ship it.                                                                            |
| [Frontend + backend](frontend-backend/workflow.yaml)               | Split the work and its interface, build the frontend and the backend at once on their own branches, test them together, review, then ship.                       |
| [Incident investigation](incident-investigation/workflow.yaml)     | Gather the evidence, find and prove the root cause for your review, fix it with a regression test, and write a blameless postmortem.                             |
| [Performance optimization](performance-optimization/workflow.yaml) | Measure a baseline you can repeat, profile to find what is actually slow, fix it, and keep the change only if the same measurement shows a real gain.            |
| [Pull request review](pull-request-review/workflow.yaml)           | Read a pull request, review it for bugs and for security on two agents at once, check every finding before you see it, then post the review once you approve it. |
| [Research report](research-report/workflow.yaml)                   | Agree the questions with you, research them from two angles at once, write one report with sources, and fact-check every claim before you get it.                |
| [Safe refactor](safe-refactor/workflow.yaml)                       | Pin today's behavior with tests first, refactor without changing it, then have another agent confirm nothing changed and no test was weakened.                   |
| [Security audit](security-audit/workflow.yaml)                     | Map the attack surface, hunt for vulnerabilities, verify each one before it is reported, and let you decide whether to fix them now.                             |
| [Technical design](technical-design/workflow.yaml)                 | Research the question, then write a design for your review. No code changes.                                                                                     |
| [Increase test coverage](test-coverage/workflow.yaml)              | Find the untested code that matters most, write tests that fail when it breaks, and have another agent check they test something real.                           |
| [Test-first feature](test-first-feature/workflow.yaml)             | Write the behavior down as a spec for your review, turn it into failing tests, then build until they pass without touching the tests.                            |
| [Design and build a UI change](ui-design-and-build/workflow.yaml)  | Draft three directions for a screen, let you pick one, build it, then check the result in light and dark and at small and large sizes before review.             |
| [Write documentation](write-documentation/workflow.yaml)           | Outline the docs from the code for your review, write them, then check every claim, command and example against the real code before they are done.              |

## Writing one

1. Make a folder named for the workflow, in lowercase with dashes, with `workflow.yaml` at its top and a short `README.md` beside it. The README is shown as plain text on the listing's page, so leave out Markdown syntax.
2. Write the file in Kettu's workflow format: `format: 1`, a `name` in English, a `description`, other languages under `locales`, and the `steps` in order, the first being the start. Each step has an `id`, a `name`, a `prompt`, who does it (`by: agent` or `you`), what it hands in (`document`, `outcome` or `note`) and its `outcomes`, each going `to` one or more steps or ending the task with `end: done` or `end: dropped`. Never name an agent, a harness or a model: whoever runs the workflow has their own.
3. Check it in Kettu: ask an agent to run `marketplace_check` on the folder, or choose Publish › From a folder in Marketplace › Published. Every problem names the field it is in.
4. Open a pull request with the folder.

## License

MIT, see [LICENSE](LICENSE).
