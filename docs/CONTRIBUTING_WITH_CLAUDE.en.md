# Your first Italia Uno contribution, with Claude

For **darklingx**, contributing to **Zhiang Wang / Team Snapper's** repository. Repository and fork names checked on **9 November 2026**. GitHub and Claude labels can change; verify the destination rather than relying on a button's position.

[中文完整手册](CONTRIBUTING_WITH_CLAUDE.md) · [Copyable Claude prompt](CLAUDE_CONTRIBUTION_PROMPT.md) · [Project contribution guide](../CONTRIBUTING.md)

## What you are trying to do

You want to send the owner a **pull request (PR)**: a proposal to include your changes. You do not need the owner's password or administrator access. You work in your own copy, and the owner decides whether to merge your work. [GitHub: PRs from forks](https://docs.github.com/en/pull-requests/how-tos/create-pull-requests/creating-a-pull-request-from-a-fork).

These are different things:

| Item | What it means |
| --- | --- |
| Fork | Your copy of the repository on GitHub. |
| Branch | A separate line of work inside a repository. |
| Commit | A saved version of a particular change. |
| Pull request | A request for the owner to review and merge your changes. |
| README credit | A manually written acknowledgment in the project documentation. |
| Contributors graph | GitHub's automatically generated commit statistics. |
| Collaborator access | Permission to write directly to the owner's repository; separate from contributing by PR. |

There is no universal **Apply to become a contributor** button. A useful change, a PR and the owner's review are the route described here.

## Keep this destination card beside you

| Field | Exact value |
| --- | --- |
| Owner's repository / upstream | **[shian493719730-art/italia_uno](https://github.com/shian493719730-art/italia_uno)** |
| Destination / base branch | **`main`** |
| Your existing fork / head repository | **[darklingx/italia_uno](https://github.com/darklingx/italia_uno)** |
| Suggested new source branch | **`docs/darklingx-contribution`** |
| Page to start a PR | **[Open the correct comparison page](https://github.com/shian493719730-art/italia_uno/compare)** |
| Page to check submitted PRs | **[Owner's pull requests](https://github.com/shian493719730-art/italia_uno/pulls)** |

The project was transferred. **Do not send your PR to `z48gdcngbf-jpg/italia_uno`**, even if older documentation or a previous comparison selects it. Check the full owner name each time.

## 1. Choose which Claude setup you have

**Ordinary Claude chat:** ask Claude to read relevant files, draft an improvement and explain the steps. If available, use **+ → Add from GitHub** to attach a small set of project files. Attaching files supplies context; do not treat it as proof that a PR was created. You can do every GitHub step below in your browser. [Anthropic: GitHub integration](https://support.claude.com/en/articles/10167454-use-the-github-integration).

**Claude Code:** it can work on a repository and help create PRs when the necessary tools, authentication and permissions are available. Use the same destination card. If a cloud session creates a PR inside your fork, that is not yet a PR to the owner's project: use the comparison steps below to target the upstream repository. Availability depends on your setup. [Claude Code workflows](https://code.claude.com/docs/en/common-workflows) · [Claude Code in the cloud](https://support.claude.com/en/articles/12618689-use-claude-code-in-the-cloud).

Start by giving Claude the [full contribution prompt](CLAUDE_CONTRIBUTION_PROMPT.md). Fill in its final **MY ACTUAL TASK** section. If you do not know which setup you have, ask it to identify its capabilities first.

## 2. Sign in to the right GitHub account

1. Open [GitHub](https://github.com/) and sign in.
2. Click your avatar at the top right. Check that the account is **darklingx**.
3. Open the [owner's repository](https://github.com/shian493719730-art/italia_uno). Its top-left owner must read **shian493719730-art**.
4. Open [your fork](https://github.com/darklingx/italia_uno). Its owner must read **darklingx**. This fork already existed when this guide was written; you do not need to delete it or make another one.

If you use a different GitHub account, substitute that account's fork for `darklingx` throughout the source-side instructions. The owner's destination stays the same.

## 3. Prepare a branch in your fork

1. In **darklingx/italia_uno**, open the branch dropdown above the file list and select **main**.
2. If GitHub says the branch is behind upstream, open **Sync fork** and review **Update branch**. If it warns about discarding your own commits or conflicts, stop and ask Claude to inspect; do not discard work just to continue. [GitHub: syncing a fork](https://docs.github.com/en/pull-requests/how-tos/work-with-forks/syncing-a-fork).
3. Open the branch dropdown again. Type **`docs/darklingx-contribution`**.
4. Select **Create branch: docs/darklingx-contribution from main**, or the equivalent create option.
5. Confirm that the dropdown now shows your new branch.

If that branch already exists, inspect it or choose a new meaningful name such as `docs/darklingx-contribution-2`. Do not overwrite it blindly. If you already made genuine changes on `patch-1`, you can use that branch instead; review its actual files before selecting it in the PR form.

## 4. Prepare one useful change with Claude

Tell Claude what you actually contributed or want to improve. Good first contributions include a documentation correction, a reproducible testing report, an authorized original asset, or a focused code fix. If your creative work already happened outside GitHub, describe it accurately and link to evidence you are allowed to share.

Do not submit a file that only says “my contribution,” invent a development role, or claim tests you did not run. A PR should give the maintainer something useful to review.

### A small concrete task you can propose

At the time this guide was written, the README still had old **Project home** and **git clone** repository URLs. If those are still wrong, you can propose correcting those two repository references to:

```text
Project home: https://github.com/shian493719730-art/italia_uno
git clone https://github.com/shian493719730-art/italia_uno.git
```

Ask Claude to identify the exact current lines before editing. Keep creator profile links, the live-game URL, credits and other content unchanged unless you have a separate reason to change them. If the repository references are already correct, choose another actual issue.

For this task, you can paste:

```text
Read the current upstream README.md. Check only its Project home repository
link and git clone repository URL. If they still point to the old owner,
show me a minimal correction to shian493719730-art/italia_uno. Keep all
creator profiles, live-game links, credits and their order unchanged.
Do not change the game or invent a contribution statement. If already
correct, tell me rather than making an unnecessary change.
```

## 5. Save the change on GitHub

For the README correction:

1. Stay in **your fork**, with **your new branch** selected.
2. Click **README.md**, then the pencil / **Edit this file** button.
3. Make only the reviewed correction. Use **Preview** and inspect the change.
4. Click **Commit changes…**.
5. Use a descriptive message, such as **Correct project repository links in README**, only if that is what you changed.
6. Confirm the destination is **your contribution branch**. Commit the changes.

For a new document instead: use **Add file → Create new file**, enter its path, paste the reviewed content, then commit it to your branch. For example, `docs/contributions/darklingx.md` is suitable only for a substantive, factual record of actual work—not a name-only placeholder. [GitHub: creating files](https://docs.github.com/en/repositories/working-with-files/managing-files/creating-new-files).

**Checkpoint:** you can see the changed file on your fork's contribution branch. Saving text in Claude alone does not create a GitHub commit.

## 6. Send a PR to the owner, not to yourself

1. Open **[this exact comparison page](https://github.com/shian493719730-art/italia_uno/compare)**.
2. Click **compare across forks** if both repositories are not visible.
3. Set these four controls. Read all four before continuing:

| GitHub control | Select |
| --- | --- |
| **base repository** | **`shian493719730-art/italia_uno`** |
| **base** | **`main`** |
| **head repository / head fork** | **`darklingx/italia_uno`** |
| **compare** | **`docs/darklingx-contribution`**, or the branch containing your actual change |

4. Review the file differences below. They should show only the intended changes. If unrelated files fill the page, pause and ask Claude to inspect the branch.
5. Click **Create pull request**.
6. Enter a meaningful title and description. Use the template below, replacing every bracketed instruction with facts.
7. Click the final **Create pull request** button. For a completed change, use a normal PR; a **Draft** means it is still work in progress.

This is GitHub's fork-to-upstream comparison process. A green comparison button by itself does not mean the request has been sent. [Official instructions](https://docs.github.com/en/pull-requests/how-tos/create-pull-requests/creating-a-pull-request-from-a-fork).

### PR description template

```markdown
## Summary
[What this change does and why it helps.]

## My contribution
[What I actually did; identify any earlier creative work separately.]

## Files changed
[List the relevant files or assets.]

## Verification
[Checks I actually performed and their results.]
[If documentation only: state that no game code changed and which links/text
I checked. Do not claim npm tests ran if they did not.]

## AI assistance
[How Claude or another tool helped; what I reviewed myself.]
```

Do not paste the template with its instructions left unfilled.

## 7. Check that it was actually sent

The resulting page must satisfy all of these:

- The address begins **`https://github.com/shian493719730-art/italia_uno/pull/`**, followed by a number.
- The PR shows your real GitHub account as its author.
- Its destination is the owner's **main**; its source is your fork's contribution branch.
- The status is **Open**, or clearly **Draft** if you intentionally made a draft.
- The **Files changed** tab contains your intended changes.

Copy that **PR URL** to Zhiang Wang. A profile, a fork homepage, a Claude conversation or a commit URL is not the same link.

Suggested message:

```text
Hi Zhiang, I submitted my contribution here: [paste the actual PR URL].
It targets shian493719730-art/italia_uno:main from darklingx:[my branch].
The change is [one factual sentence]. Please review it when convenient.
```

If Claude says “done,” ask it for the actual PR URL and open the page yourself. If it cannot provide one, follow the remaining browser steps.

## 8. Review, corrections and contribution credit

The owner may request changes. Edit and commit on the **same source branch** to update that PR; do not open another request for each correction. The owner decides when to merge. The PR page changes to **Merged** when that happens.

For GitHub's **Contributors graph**, commits must reach the default branch and their author email must be linked to your account. The graph excludes empty and merge commits and shows the top 100 contributors. It cannot be manually arranged to put a person last. README acknowledgments are separate. [GitHub's graph rules](https://docs.github.com/en/repositories/viewing-activity-and-data-for-your-repository/viewing-a-projects-contributors).

If you commit locally, check your author email before the commit. Use your own verified address or the **exact** private noreply address shown in [GitHub Settings → Emails](https://github.com/settings/emails). Do not copy the owner's address or guess yours. [GitHub: commit email](https://docs.github.com/en/account-and-profile/how-tos/email-preferences/setting-your-commit-email-address).

## 9. Common problems

| What you see | What to do |
| --- | --- |
| **Nothing to compare** | Check the four comparison fields. Ensure your changes were committed to the selected source branch and, if using local tools, pushed. Check whether the same work is already merged or has an existing PR. |
| PR address contains **z48gdcngbf-jpg** | It went to the old destination. Open the correct comparison page and propose your branch to **shian493719730-art/italia_uno:main**. Tell the maintainer which new PR replaces it. |
| PR address contains **darklingx** | You proposed changes inside your own fork. Open the owner's comparison page and select the correct base repository. |
| Permission denied when pushing to the owner's repo | Push to **your fork** and submit a PR. Direct owner-repository access is not required for this route. |
| GitHub asks to discard commits during sync | Do not discard them. Ask Claude to inspect and preserve the existing work, or use a new local branch from upstream as described below. |
| Many unrelated changes or merge conflicts | Ask Claude to inspect the branch history and propose a focused fix. Do not force-push or reset work to make the warning disappear. |
| Claude produced a file but there is no PR | Commit and push it to your fork, then complete section 6. |
| PR is **Closed**, not **Merged** | It was not incorporated by that PR. Read the discussion or ask the owner what needs changing. |
| Name still missing from the graph | Check default-branch merge, commit author email and selected graph date range; GitHub may need time to refresh. A README credit or open PR alone does not satisfy the graph rules. |

## Optional: local Claude Code / GitHub CLI route

Skip this section if you used the browser steps. It is for people who already have Git, Claude Code and GitHub CLI installed. Ask Claude to perform and explain it using the [full prompt](CLAUDE_CONTRIBUTION_PROMPT.md); do not install tools just to complete a documentation PR.

In a **fresh working folder**, clone your fork, fetch the upstream and create a branch from the owner's current `main`:

```sh
git clone https://github.com/darklingx/italia_uno.git italia-uno-contribution
cd italia-uno-contribution
git remote add upstream https://github.com/shian493719730-art/italia_uno.git
git fetch upstream
git switch -c docs/darklingx-contribution upstream/main
```

If the folder, remote or branch already exists, inspect it instead of deleting or replacing it. These commands are for a fresh clone. Confirm that GitHub CLI is signed in as **darklingx**, and that Git's author identity is yours; signing in to GitHub and configuring Git authorship are separate steps. Never paste passwords or tokens into a chat.

After completing and reviewing the actual change, stage only its intended files, inspect the staged diff, and make a descriptive commit. Then:

```sh
git push -u origin docs/darklingx-contribution
gh pr create --repo shian493719730-art/italia_uno --base main --head darklingx:docs/darklingx-contribution --web
```

The final command opens the browser form; **finish submitting it** and verify the resulting PR URL. If your branch name differs, substitute it in both commands. `--repo`, `--base` and the owner-qualified `--head` explicitly select the target and source. [GitHub CLI reference](https://cli.github.com/manual/gh_pr_create).

For code changes, consult the current `package.json` and project instructions. This snapshot provides `npm test`, `npm run typecheck` and `npm run build`; install dependencies with `npm ci` and use Node.js 22.13+ as specified by the project. Run checks appropriate to what changed and report actual results. Documentation-only work does not require a game rebuild.

## Final checklist

- [ ] I used my own GitHub account and a real, useful contribution.
- [ ] I preserved existing credits and their order.
- [ ] I reviewed the changed files and reported verification truthfully.
- [ ] The PR targets **shian493719730-art/italia_uno → main**.
- [ ] I opened the actual PR page and checked its author, source and status.
- [ ] I sent Zhiang the **PR URL**, rather than my fork or profile link.
- [ ] I understand the owner reviews and merges; credit statistics are a later, separate check.
