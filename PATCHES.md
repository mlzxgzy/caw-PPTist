# CAW 分支定制登记（PATCHES）

> 本文件登记 `CAW` 分支相对上游 `master` 的全部定制。每次上游同步
> （`git merge master → CAW`）发生冲突时，以本表为裁决依据。
> 详细背景见宿主仓库 `course-agent-workbench/docs/pptist-integration-spec.md`。

| # | 文件 | 定制内容 | 原因 | 冲突策略 |
|---|---|---|---|---|
| 1 | `src/services/index.ts` | `SERVER_URL` 固定为 `'/api'`（原：dev 走 /api、prod 走 server.pptist.cn） | AI 服务由宿主后端实现同协议端点接管，生产环境不能指向外部服务器 | 保留 CAW 侧 |
