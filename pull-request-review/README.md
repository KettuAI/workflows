Use it when you want a thorough second look at a pull request someone else wrote, or one an agent wrote for you, without changing any code.

1. Scope reads the pull request and its diff and notes what it touches and where problems are likely.
2. Correctness review and Security review run at the same time, so two agents look for different kinds of problems.
3. Verify and consolidate tries to prove every finding wrong, drops the false ones and writes the review as a document. You approve it or send it back with comments.
4. Post the review puts the approved review on the pull request. It never approves or merges.

Name the pull request in the requirement, for example Review https://github.com/owner/repo/pull/123. Posting needs the GitHub CLI signed in.
