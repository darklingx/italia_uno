# Prompt: help me contribute to Italia Uno

[English handbook](CONTRIBUTING_WITH_CLAUDE.en.md) · [中文手册](CONTRIBUTING_WITH_CLAUDE.md)

Copy the block below into Claude. Replace the final task description with work you actually intend to do. The default GitHub account is `darklingx`; change that account and fork if a different person uses this prompt.

```text
Help me submit a genuine contribution to the Italia Uno project.
Guide me in small steps; explain GitHub labels in plain language.

IDENTITY AND DESTINATION
- I am GitHub user darklingx. Verify the authenticated account before writing.
- Canonical upstream: https://github.com/shian493719730-art/italia_uno
- PR destination: shian493719730-art/italia_uno, base branch main.
- My existing fork: https://github.com/darklingx/italia_uno
- Suggested NEW source branch: docs/darklingx-contribution.
- Do not send the PR to z48gdcngbf-jpg/italia_uno or to my own fork.
- Read the upstream CONTRIBUTING.md and applicable project instructions first.

FIRST IDENTIFY YOUR CAPABILITIES
1. State whether this session can only read/draft, can edit local files,
   can push to my fork, and can actually create a GitHub PR.
2. Do not assume that attaching GitHub files to a chat grants write access.
3. If you cannot perform a step, give me its exact browser steps instead.
   Never report a commit, push, PR or test as completed without evidence.

SCOPE AND AUTHORSHIP
- Help with a real, useful change: code, docs, authorized assets, an actual
  test report, or a factual account of creative work I really performed.
- Do not invent my past work, test results, titles, sources or team roles.
- Do not create a name-only "contribution" file, an empty commit, or use
  somebody else's identity to make the Contributors graph show my name.
- Preserve existing credits and their order. Explain AI assistance truthfully.
- Keep the task focused. Do not change gameplay, branding or deployment
  unless the actual task below calls for that change.

IF CODING / GIT TOOLS ARE AVAILABLE
1. Inspect git status, branches and remotes before changing anything.
   Preserve existing work. Do not delete forks, reset files, force-push,
   or rewrite commit history.
2. Work from current upstream main on a new branch in my fork. If using
   an existing contribution branch, first inspect its actual diff.
3. Check the Git author email is associated with MY GitHub account.
   Ask me to copy my own noreply address from GitHub Settings > Emails
   if needed; do not guess it or request a password/token in chat.
4. Make only the agreed change and show me the diff.
5. Perform checks appropriate to the change. For documentation, verify
   accuracy and links. For code, consult package.json and run relevant
   checks. Record exactly what ran; do not invent passes.
6. Commit as the actual contributor, push to darklingx/italia_uno,
   then propose a PR to shian493719730-art/italia_uno:main.
7. For the browser comparison, use:
   base repository = shian493719730-art/italia_uno
   base branch = main
   head repository = darklingx/italia_uno
   compare branch = the actual branch containing my pushed changes.
8. Before submitting, check for an existing PR from this branch. Do not
   create duplicates. Follow any tool permission prompts in my environment.
9. Do not merge the PR or change repository access settings for the owner.

FINISH WITH EVIDENCE
Return:
- the actual files changed and what I contributed;
- checks performed and anything not checked;
- the commit SHA and pushed branch, if actually created;
- the REAL PR URL, if actually opened, beginning with
  https://github.com/shian493719730-art/italia_uno/pull/
- the actual status: not submitted / open / draft / merged.
If blocked, identify the exact next step instead of saying "done".

MY ACTUAL TASK:
[Replace this line with your real intended contribution and relevant evidence.
If unsure, first suggest one small verified issue in the current repo;
do not submit until I have chosen the task.]
```

If Claude has prepared changes but you cannot tell whether they were sent, paste:

```text
Please verify, without making additional changes: what is the exact PR URL,
base repository, base branch, head repository, source branch and status?
Show the evidence you can access. If no PR exists, say so and give me the
remaining steps. A local file or commit is not proof of an opened PR.
```
