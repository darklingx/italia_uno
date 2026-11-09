# 使用 Claude 向 Italia Uno 提交贡献：完整新手手册

适用对象：GitHub 用户 **darklingx**，向 **Zhiang Wang / Team Snapper** 的项目提交贡献。仓库与 Fork 信息核对日期：**2026 年 11 月 9 日**。界面位置可能变化，请以仓库全名为准。

[English handbook](CONTRIBUTING_WITH_CLAUDE.en.md) · [可复制给 Claude 的完整提示词](CLAUDE_CONTRIBUTION_PROMPT.md) · [项目贡献入口](../CONTRIBUTING.md)

## 先明白最终要做什么

你需要向项目负责人发一个 **Pull Request，简称 PR**，意思是“请审核并把我的改动合并进你的项目”。你在自己的副本上操作，负责人审核后决定是否合并；不需要对方的密码或管理员权限。[GitHub 官方说明](https://docs.github.com/en/pull-requests/how-tos/create-pull-requests/creating-a-pull-request-from-a-fork)。

| 名称 | 简单解释 |
| --- | --- |
| Fork | GitHub 上属于你自己的项目副本。 |
| Branch / 分支 | 在同一个仓库中单独开展某项改动。 |
| Commit / 提交 | 保存一版具体改动。 |
| Pull Request / PR | 请求负责人审核并接纳这些改动。 |
| README 署名 | 人工写在说明文档中的致谢。 |
| Contributors 图表 | GitHub 根据提交记录自动统计的页面。 |
| Collaborator 权限 | 直接写入对方仓库的权限，与通过 PR 贡献是两回事。 |

GitHub 没有一个通用的“申请成为 Contributor”按钮。这份手册教你完成的是：**真实改动 → 提交 → PR → 负责人审核与合并**。

## 重要：把这张表放在旁边对照

| 要确认的项目 | 必须使用的内容 |
| --- | --- |
| 负责人的仓库 / upstream | **[shian493719730-art/italia_uno](https://github.com/shian493719730-art/italia_uno)** |
| 接收改动的分支 / base | **`main`** |
| 你自己的 Fork / head | **[darklingx/italia_uno](https://github.com/darklingx/italia_uno)** |
| 建议新建的工作分支 | **`docs/darklingx-contribution`** |
| 正确的 PR 比较入口 | **[点这里进入](https://github.com/shian493719730-art/italia_uno/compare)** |
| 查看有没有发成功 | **[负责人的 PR 列表](https://github.com/shian493719730-art/italia_uno/pulls)** |

项目已经转交过。**不要发到 `z48gdcngbf-jpg/italia_uno`**，即使旧文档或上次的页面还选着它。每次都读一遍地址里的 owner。

## 第一步：判断你用的是哪种 Claude

**普通 Claude 聊天：**可以让它阅读资料、准备文字或修改建议。如果界面有 **+ → Add from GitHub**，可以添加少量相关文件作为上下文。添加文件不等于已经发出 PR；下面的 GitHub 操作都可以由你在浏览器完成。[Claude 官方 GitHub 集成说明](https://support.claude.com/en/articles/10167454-use-the-github-integration)。

**Claude Code：**在具备工具、账号认证和权限时，可以协助修改仓库、提交及创建 PR。仍须使用上面的目标仓库。如果云端任务只在你自己的 Fork 中建了 PR，还需要按照后文比较步骤发到负责人的仓库。不同环境的能力不同。[Claude Code 工作流](https://code.claude.com/docs/en/common-workflows) · [云端使用说明](https://support.claude.com/en/articles/12618689-use-claude-code-in-the-cloud)。

先把[这份完整提示词](CLAUDE_CONTRIBUTION_PROMPT.md)复制给 Claude，填好最后的 **MY ACTUAL TASK**。不确定版本时，让它先说明自己能否读文件、改文件、推送、真正创建 PR。

## 第二步：登录自己的 GitHub，找到正确仓库

1. 打开 [GitHub](https://github.com/)，登录你自己的账号。
2. 点右上角头像，确认用户名是 **darklingx**。
3. 打开[负责人的仓库](https://github.com/shian493719730-art/italia_uno)，左上角 owner 必须是 **shian493719730-art**。
4. 再打开[你自己的 Fork](https://github.com/darklingx/italia_uno)，左上角 owner 必须是 **darklingx**。核对时这个 Fork 已存在，不用删除或重新创建。

如果你实际使用另一个 GitHub 账号，后文“你自己的 Fork”要换成那个账号的副本；接收改动的负责人仓库不变。

## 第三步：在自己的 Fork 中准备工作分支

1. 在 **darklingx/italia_uno** 文件列表上方找到分支下拉菜单，先选 **main**。
2. 如果提示落后于原仓库，点 **Sync fork**，查看 **Update branch**。如果出现要丢弃你的提交、冲突等提示，先停下来让 Claude 查看，不要为了同步删除已有工作。[GitHub 同步说明](https://docs.github.com/en/pull-requests/how-tos/work-with-forks/syncing-a-fork)。
3. 再点分支下拉菜单，输入 **`docs/darklingx-contribution`**。
4. 点击类似 **Create branch: docs/darklingx-contribution from main** 的创建选项。
5. 创建后，检查下拉菜单显示的已经是这个新分支。

如果这个名字已经存在，先检查内容，或改用 `docs/darklingx-contribution-2`，不要覆盖。你如果已经在 `patch-1` 中完成了真实改动，也可以用它，但必须先查看里面到底改了什么。

## 第四步：让 Claude 帮你准备一项真实改动

告诉 Claude 你实际做过或准备改进的内容。文档纠错、可复现的实际测试报告、自己有权公开的原创素材、具体代码修复，都可以成为贡献。如果创意工作之前发生在 GitHub 之外，可以准确记录它，并附上允许分享的证据。

不要只建一个写着“我贡献了”的文件，不要编造开发分工或测试结果。负责人需要看到一项有实际用途、可以审核的改动。

### 一个可以直接提议的小任务

写手册时，README 中的 **Project home** 和 **git clone** 仓库地址仍指向旧账号。开始操作时如果还是错误的，可以提议仅修正这两处仓库引用：

```text
Project home: https://github.com/shian493719730-art/italia_uno
git clone https://github.com/shian493719730-art/italia_uno.git
```

先让 Claude 检查当前内容。创作者个人主页、在线游戏地址、贡献者署名与排序等，不属于这项修改。如果两处已经修好，就选择另一项真实问题，不要重复制造改动。

可复制给 Claude：

```text
请读取当前 upstream 的 README.md，只检查 Project home 的项目仓库链接
和 git clone 地址。如果仍指向旧 owner，请展示改为
shian493719730-art/italia_uno 的最小修改。
保持创作者个人主页、在线游戏链接、贡献者内容及排序不变。
不要修改游戏，也不要编造我的贡献说明。如果已经正确，请告诉我。
```

## 第五步：把改动保存到自己的 GitHub 分支

如果做的是 README 纠错：

1. 留在 **自己的 Fork**，并确认已选中 **自己的工作分支**。
2. 点击 **README.md**，再点铅笔图标 / **Edit this file**。
3. 只修改刚才审核过的地方；用 **Preview** 检查。
4. 点击 **Commit changes…**。
5. 填写准确的提交说明。例如确实修正了仓库链接，才写 **Correct project repository links in README**。
6. 确认保存到的是 **你的工作分支**，然后提交。

如果要新建文档：点 **Add file → Create new file**，填写文件路径、粘贴审核后的内容，再提交到你的分支。例如 `docs/contributions/darklingx.md` 只适用于有实质内容的真实工作记录，不是仅仅写名字的占位文件。[GitHub 新建文件说明](https://docs.github.com/en/repositories/working-with-files/managing-files/creating-new-files)。

**这一步完成的标志：**在你自己 Fork 的工作分支里，能看到已经改好的文件。只在 Claude 对话里生成文字，还不算 GitHub 提交。

## 第六步：发起 PR，四个下拉框逐一核对

1. 打开[这个正确的比较页面](https://github.com/shian493719730-art/italia_uno/compare)。
2. 如果看不到两个仓库选择，点 **compare across forks**。
3. 按下面的表逐一选择，四项全部核对：

| 页面上的英文标签 | 应选择 |
| --- | --- |
| **base repository** | **`shian493719730-art/italia_uno`** |
| **base** | **`main`** |
| **head repository / head fork** | **`darklingx/italia_uno`** |
| **compare** | **`docs/darklingx-contribution`**，或确实包含你改动的分支 |

4. 看下面的文件差异，应该只有你打算提交的改动。大量无关文件出现时，先让 Claude 检查，不要直接继续。
5. 点击 **Create pull request**。
6. 写清标题与描述。可用下面模板，但要把方括号里的提示全部替换成事实。
7. 点击最后的 **Create pull request** 才是正式发出。完成的改动用普通 PR；**Draft** 表示还未准备好。

上面是 GitHub 的 Fork → 原仓库提交流程。仅看到绿色比较按钮，不代表已经发送。[GitHub 官方步骤](https://docs.github.com/en/pull-requests/how-tos/create-pull-requests/creating-a-pull-request-from-a-fork)。

### PR 描述模板

```markdown
## Summary
[这次具体改了什么，解决什么问题。]

## My contribution
[我实际做了什么；如果描述此前创意工作，要与这次文件修改区分。]

## Files changed
[涉及哪些文件或素材。]

## Verification
[实际做过的检查及结果。]
[纯文档修改说明没有改游戏代码，并列明核对了什么。
没有运行 npm 测试就不要写通过。]

## AI assistance
[Claude 或其他工具协助了什么，自己审核了什么。]
```

## 第七步：判断到底有没有发成功

打开创建后的 PR 页面，必须同时满足：

- 地址以 **`https://github.com/shian493719730-art/italia_uno/pull/`** 开头，后面有一个数字编号。
- 作者是你真实登录的 GitHub 账号。
- 接收方是负责人仓库的 **main**；来源是你 Fork 中的工作分支。
- 状态是 **Open**；如果你主动建了草稿，则明确显示 **Draft**。
- **Files changed** 中能看到你期望提交的文件。

把这个 **PR 页面链接**发给 Zhiang Wang。个人主页、Fork 首页、Claude 对话、单个 Commit 链接，都不是同一种链接。

可以这样发：

```text
我已经提交 PR：[粘贴实际 PR 链接]
接收方是 shian493719730-art/italia_uno:main，
来源是 darklingx:[实际分支名]。
这次修改是：[一句话准确描述]。请审核。
```

如果 Claude 只说“完成”，继续问它“实际 PR 链接是什么”，并自己点开检查。没有链接就不能据此认定已提交。

## 第八步：等待负责人审核与合并

负责人可能要求修改。继续在 **同一个来源分支**里编辑并提交，就会更新同一个 PR，不必每改一次都新建 PR。负责人决定是否合并；页面显示 **Merged** 才表示这个 PR 已合并。

GitHub 的 **Contributors 图表**要求提交进入默认分支，且作者邮箱关联本人账号；空提交与合并提交本身不计入，图表显示前 100 名贡献者。它不能人工设置某个人“排最后”。README 的人工署名是另一回事。[GitHub 图表规则](https://docs.github.com/en/repositories/viewing-activity-and-data-for-your-repository/viewing-a-projects-contributors)。

本地提交时，提前确认 Git 作者邮箱。用本人已验证邮箱，或从 [GitHub Settings → Emails](https://github.com/settings/emails) 复制本人**完整、准确**的 noreply 邮箱；不要用负责人的邮箱，也不要猜自己的邮箱。[GitHub 提交邮箱说明](https://docs.github.com/en/account-and-profile/how-tos/email-preferences/setting-your-commit-email-address)。

## 遇到问题时对照这里

| 问题 | 下一步 |
| --- | --- |
| **Nothing to compare** | 检查四个比较选项；确认改动已提交到所选分支。本地操作还要 push。也要查是否已有 PR 或已经合并。 |
| PR 地址里是 **z48gdcngbf-jpg** | 发到旧目的地了。回到正确比较入口，把同一真实改动分支发给 **shian493719730-art/italia_uno:main**，并告诉负责人新 PR 替代哪一个。 |
| PR 地址里是 **darklingx** | 只在自己的 Fork 内申请合并了。改用负责人仓库的比较入口。 |
| 不能直接 push 到负责人仓库 | 这是正常的权限区别。推送到自己的 Fork，再发 PR。 |
| 同步要求丢弃提交 | 不要丢弃。让 Claude 检查并保留现有工作；必要时从 upstream 另建工作分支。 |
| 大量无关改动或冲突 | 让 Claude 查看分支历史并提出最小修复，不要强推或清空文件来消除提示。 |
| Claude 给了文件，但没有 PR | 还没完成提交。先保存并推送到 Fork，再做第六步。 |
| 状态是 **Closed**，没有 **Merged** | 这个 PR 没有被合并。阅读讨论，询问负责人需要怎么调整。 |
| 图表还没出现名字 | 核对默认分支是否合并、作者邮箱、图表时间范围，并留出刷新时间。README 署名或一个 Open PR 本身不满足图表条件。 |

## 可选：已经使用本地 Claude Code 的人

浏览器操作完成后可以跳过这里。这一节适用于已经安装 Git、Claude Code 与 GitHub CLI 的人，不必为了文档 PR 专门安装。把[完整提示词](CLAUDE_CONTRIBUTION_PROMPT.md)交给 Claude，让它逐步解释并操作。

在**全新的工作目录**克隆自己的 Fork，从负责人当前的 main 建立工作分支：

```sh
git clone https://github.com/darklingx/italia_uno.git italia-uno-contribution
cd italia-uno-contribution
git remote add upstream https://github.com/shian493719730-art/italia_uno.git
git fetch upstream
git switch -c docs/darklingx-contribution upstream/main
```

如果目录、remote 或分支已存在，先检查，不能照着删除或覆盖。这组命令适用于新克隆。确认 GitHub CLI 登录的是 **darklingx**，且 Git 作者身份是本人：账号登录与提交作者配置是两件事。不要把密码或 token 粘贴进聊天。

完成真实修改后，只暂存相关文件，检查暂存差异，写准确说明并 commit。然后：

```sh
git push -u origin docs/darklingx-contribution
gh pr create --repo shian493719730-art/italia_uno --base main --head darklingx:docs/darklingx-contribution --web
```

最后一条命令打开浏览器表单，**仍需完成提交**并检查最终链接。实际分支名不同就同时修改两条命令。`--repo`、`--base` 和带账号的 `--head` 用来明确接收方和来源。[GitHub CLI 官方说明](https://cli.github.com/manual/gh_pr_create)。

代码修改应读取当前 `package.json` 及项目要求。此版本提供 `npm test`、`npm run typecheck`、`npm run build`，用 `npm ci` 安装依赖，项目要求 Node.js 22.13+。根据实际改动运行相应检查，只报告真实结果。仅修改文档无需重建游戏。

## 交给负责人之前，最后勾选

- [ ] 用的是自己的 GitHub 账号，提交的是有实际用途的工作。
- [ ] 没有改变原有贡献者内容或排序。
- [ ] 检查过文件差异，检查结果与 AI 使用说明属实。
- [ ] PR 接收方是 **shian493719730-art/italia_uno → main**。
- [ ] 打开实际 PR 页面核对了作者、来源分支和状态。
- [ ] 发给 Zhiang 的是 **PR 链接**，不是个人主页或 Fork 首页。
- [ ] 明白负责人审核并合并后，还需另行核对贡献统计。
