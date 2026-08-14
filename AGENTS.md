# 项目约定（AGENTS.md）

本文件是所有协作者（包括 AI 编码助手）必须遵守的规则。修改本仓库任何文件前，请先阅读并遵守以下约定。

## 项目简介

- 内容：贪吃蛇网页游戏
- 技术栈：纯前端（HTML + CSS + JavaScript），游戏代码集中在单个 HTML 文件，无构建步骤、无第三方依赖
- 在线地址（最新版）：https://aaaaaaaalh.github.io/hungry-snake/snake-game/

## 目录结构

| 路径 | 说明 |
| --- | --- |
| `snake-game/index.html` | **最新版**游戏代码（唯一需要修改的代码文件） |
| `snake-game/README.md` | 最新版游戏说明（运行方式、操作玩法） |
| `versions/vX.Y.Z/` | 历史版本存档：每个已发布版本一个文件夹，可独立运行 |
| `CHANGELOG.md` | 版本变更记录：每个版本相对上一个版本改了什么 |
| `README.md`（根目录） | 仓库总览与文件索引 |
| `AGENTS.md` | 本文件：项目约定 |
| `.nojekyll`（根目录） | 禁止 Jekyll 处理（Pages 部署必需，勿删） |

## 版本约定

1. 新版本统一整合进同一仓库、同一 `snake-game/` 目录迭代，**不单独开新仓库**。
2. 版本号遵循语义化版本（主.次.修订），例如 v1.1.0：
   - 新增功能 → 次版本 +1（v1.0.0 → v1.1.0）
   - 修复 bug → 修订号 +1（v1.1.0 → v1.1.1）
   - 大改动或不兼容变更 → 主版本 +1（v1.x → v2.0.0）
3. 每个新版本发布时必须按以下顺序执行：
   - 更新 `snake-game/` 中的游戏代码
   - **复制存档**：将 `snake-game/index.html` 和 `snake-game/README.md` 完整复制到 `versions/vX.Y.Z/`（新版本号文件夹）
   - 更新 `CHANGELOG.md`，在文件顶部按格式新增一条版本记录（新增 / 修改 / 修复）
   - 打对应 git tag：`git tag vX.Y.Z`
4. `versions/` 目录**只增不改**：已发布的版本存档文件永远不要修改，保证历史版本可随时回退。
5. `snake-game/` 永远是当前最新版，线上网址展示的也是它。
6. `README.md` 只描述当前最新版，不写历史版本信息；历史记录一律放 `CHANGELOG.md`。

## 版本回退

需要把线上游戏回退到某个旧版本时：

1. 用该版本存档覆盖最新版：把 `versions/vX.Y.Z/index.html` 和 `README.md` 复制回 `snake-game/`
2. 更新 `CHANGELOG.md`，记录这次回退（如：回退到 vX.Y.Z）
3. 提交并推送：`git push`，线上自动变为该版本

## 提交约定

- 提交信息用简短中文概括改动，例如：`v1.1.0 新增障碍物模式`、`Fix 快速转向反向问题`、`Update CHANGELOG`
- 每次修改游戏代码后，同步在 `CHANGELOG.md` 中添加或更新对应版本条目
- 推送代码：`git push`；推送 tag：`git push --tags`

## 部署约定

- 使用 GitHub Pages **分支部署**（Build and deployment → Source: Deploy from a branch），不依赖 GitHub Actions
- 部署设置：Branch = `master`，目录 = `/ (root)`（GitHub 分支部署仅支持根目录或 /docs）
- 在线地址：
  - 最新版：https://aaaaaaaalh.github.io/hungry-snake/snake-game/
  - 历史版本（免费附带）：https://aaaaaaaalh.github.io/hungry-snake/versions/vX.Y.Z/
- 每次 push 到 master 后 GitHub 会自动重新构建发布，无需手动操作
- 根目录的 `.nojekyll` 文件不能删除，用于禁止 Jekyll 干扰静态页面
