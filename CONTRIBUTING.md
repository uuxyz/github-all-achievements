# 两个账号协作记录

本仓库由 [uuxyz](https://github.com/uuxyz) 维护；[uyuuyuu](https://github.com/uyuuyuu) 可参与核对和补充成就资料。

## 提交与核对

1. 每次更新说明对应的成就、操作链接和 GitHub 主页上的实际结果。
2. 共同完成的修改在提交消息末尾添加 `Co-authored-by`，邮箱必须属于共同作者的 GitHub 账号。单独完成的修改只署自己的名字。
3. 通过 PR 合并修改，保留可追溯的审阅与协作记录。
4. 成就显示可能晚于操作发生时间；只在个人主页出现后标记为“已获得”。

GitHub 对共同署名的格式有[正式文档](https://docs.github.com/en/pull-requests/how-tos/commit-changes/creating-a-commit-with-multiple-authors)。

## 区分登录、PR 作者和共同署名

这三种身份需要分别核对。`gh api user --jq .login` 显示当前 CLI 使用的账号；`gh pr view 编号 --json author,commits` 显示 PR 发起者和提交信息。`Co-authored-by` 只给某次提交增加共同署名，不会把该账号变成 PR 发起者或仓库协作者。

需要验证某账号实际发起 PR 时，应切换到该账号，使用它可写的 fork 提交分支，然后向原仓库发起 PR。

## 核对审查状态

PR 页面上的“请求审查”与已经完成的审查是两个不同事件。请求审查后，仍需查看 Reviews 区域是否出现批准、要求修改或评论。用 `gh pr view 编号 --json reviewRequests,reviews` 可以分别查询待处理的审查请求和已提交的审查记录。

合并前应自行检查改动是否安全、准确。成就描述中的“未经代码审查”只说明 GitHub 没有记录审查结果，不应代替必要的人工检查。
