# hungry-snake · 贪吃蛇 🐍

一个纯前端、单文件的贪吃蛇网页游戏，无需安装任何依赖，双击即可游玩。

- 🎮 在线试玩：https://aaaaaaaalh.github.io/hungry-snake/
- 📦 源码仓库：https://github.com/aaaaaaaalh/hungry-snake
- 📝 版本记录：`CHANGELOG.md`
- 📏 项目约定：`AGENTS.md`（协作者必读）

## 仓库文件说明

| 路径 | 说明 |
| --- | --- |
| `snake-game/index.html` | 游戏全部代码：界面 + 逻辑都在这个单文件里 |
| `snake-game/README.md` | 最新版游戏的操作说明（按键、玩法） |
| `CHANGELOG.md` | 版本变更记录：每个版本相对上一个版本改了什么 |
| `AGENTS.md` | 项目约定：版本规则、提交规范、部署规则 |
| `.github/workflows/pages.yml` | GitHub Actions 工作流：push 后自动发布到 GitHub Pages |

## 版本规则（速览）

- 新版本整合进 `snake-game/` 迭代，不单独开仓库
- 版本号 `v主.次.修订`：新增功能 / 修 bug / 大改动分别递增对应位
- 每个版本更新 `CHANGELOG.md` 并打 git tag
- 完整规则见 `AGENTS.md`

## 快速上手

1. 本地运行：双击 `snake-game/index.html` 或用浏览器打开
2. 提交新版本：
   ```powershell
   cd D:\cheny\Documents\cangku
   git add .
   git commit -m "更新说明"
   git push            # 自动部署，tag 需额外执行 git push --tags
   ```
