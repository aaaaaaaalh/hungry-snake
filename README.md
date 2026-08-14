# hungry-snake · 贪吃蛇 🐍

一个纯前端、单文件的贪吃蛇网页游戏，支持多账号注册登录、背景音乐、音效和 MP3 音乐库。每个账号可自定义头像和昵称，数据完全独立。无需安装任何依赖，双击即可游玩。

- 🎮 在线试玩（最新版）：https://aaaaaaaalh.github.io/hungry-snake/snake-game/
- 📦 源码仓库：https://github.com/aaaaaaaalh/hungry-snake
- 📝 版本记录：`CHANGELOG.md`
- 📏 项目约定：`AGENTS.md`（协作者必读）

## 仓库文件说明

| 路径 | 说明 |
| --- | --- |
| `snake-game/index.html` | **最新版**游戏代码：界面 + 逻辑 + 音效都在这个单文件里 |
| `snake-game/README.md` | 最新版游戏的操作说明（按键、玩法、账号） |
| `versions/` | 历史版本存档：每个已发布版本一个文件夹，可独立运行、可在线访问 |
| `CHANGELOG.md` | 版本变更记录：每个版本相对上一个版本改了什么 |
| `AGENTS.md` | 项目约定：版本规则、提交规范、部署规则 |
| `.nojekyll` | 禁止 Jekyll 处理（Pages 部署必需，勿删） |

## 版本存档

每个已发布版本都保留在 `versions/` 目录，可在 GitHub 上直接查看，也可在线游玩：

| 版本 | 说明 | 在线地址 |
| --- | --- | --- |
| v4.0.0 | 当前最新版：MP3 音乐库（公共库 + 私人库） | https://aaaaaaaalh.github.io/hungry-snake/versions/v4.0.0/ |
| v3.0.0 | 背景音乐 + 音效 | https://aaaaaaaalh.github.io/hungry-snake/versions/v3.0.0/ |
| v2.0.0 | 账号系统 | https://aaaaaaaalh.github.io/hungry-snake/versions/v2.0.0/ |
| v1.0.0 | 初始版：基础贪吃蛇 | https://aaaaaaaalh.github.io/hungry-snake/versions/v1.0.0/ |

## 版本规则（速览）

- 新版本整合进 `snake-game/` 迭代，`versions/` 只增不改
- 每个新版本 = 改代码 → 复制存档到 `versions/vX.Y.Z/` → 更新 CHANGELOG → 打 git tag
- 回退版本 = 把 `versions/vX.Y.Z/` 的文件复制回 `snake-game/`，提交推送即可
- 完整规则见 `AGENTS.md`

## 快速上手

1. 本地运行：双击 `snake-game/index.html` 或用浏览器打开
2. 提交新版本：
   ```powershell
   cd D:\cheny\Documents\cangku
   git add .
   git commit -m "vX.Y.Z 更新说明"
   git push
   git tag vX.Y.Z
   git push --tags
   ```
3. 查看战绩 / 切换账号：游戏中点击右上角头像
4. 开关声音：右上角 🔊 按钮
5. 自定义音乐：右上角 🎵 打开音乐库，上传 MP3 到公共库或私人库并选用
