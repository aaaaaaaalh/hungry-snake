# 项目约定（AGENTS.md）

本文件是所有协作者（包括 AI 编码助手）必须遵守的规则。修改本仓库任何文件前，请先阅读并遵守以下约定。

## 项目简介

- 内容：贪吃蛇网页游戏
- 技术栈：纯前端（HTML + CSS + JavaScript），游戏代码集中在单个 HTML 文件，无构建步骤、无第三方依赖
- 在线地址：https://aaaaaaaalh.github.io/hungry-snake/

## 目录结构

| 路径 | 说明 |
| --- | --- |
| `snake-game/index.html` | 游戏全部代码（唯一需要修改的代码文件） |
| `snake-game/README.md` | 当前最新版游戏说明（运行方式、操作玩法） |
| `CHANGELOG.md` | 版本变更记录：每个版本相对上一个版本改了什么 |
| `README.md`（根目录） | 仓库总览与文件索引 |
| `AGENTS.md` | 本文件：项目约定 |
| `.github/workflows/pages.yml` | GitHub Actions：push 后自动部署到 GitHub Pages |

## 版本约定

1. 新版本统一整合进同一仓库、同一 `snake-game/` 目录迭代，**不单独开新仓库**。
2. 版本号遵循语义化版本（主.次.修订），例如 v1.1.0：
   - 新增功能 → 次版本 +1（v1.0.0 → v1.1.0）
   - 修复 bug → 修订号 +1（v1.1.0 → v1.1.1）
   - 大改动或不兼容变更 → 主版本 +1（v1.x → v2.0.0）
3. 每个新版本发布时必须：
   - 更新 `CHANGELOG.md`，在文件顶部按格式新增一条版本记录（新增 / 修改 / 修复）
   - 打对应 git tag：`git tag v1.1.0`
4. 正常情况下不需要保留旧版；如需保留可玩旧版，将旧版复制到 `versions/v1.0.0/` 存档目录。
5. `README.md` 只描述当前最新版，不写历史版本信息；历史记录一律放 `CHANGELOG.md`。

## 提交约定

- 提交信息用简短中文概括改动，例如：`Add 障碍物模式`、`Fix 快速转向反向问题`、`Update CHANGELOG`
- 每次修改游戏代码后，同步在 `CHANGELOG.md` 中添加或更新对应版本条目
- 推送代码：`git push`；推送 tag：`git push --tags`

## 部署约定

- 代码推送到 `master` 分支后，由 GitHub Actions 自动部署到 GitHub Pages，无需手动操作
- 部署规则：`snake-game/` 目录内容发布到站点根目录，访问 https://aaaaaaaalh.github.io/hungry-snake/ 直接是游戏
- 仓库 Pages 设置中的 Source 必须保持为 "GitHub Actions"，不要改成 "Deploy from a branch"
