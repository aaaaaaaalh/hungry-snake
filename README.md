# hungry-snake · 贪吃蛇 🐍

一个纯前端、单文件的贪吃蛇网页游戏，支持多账号注册登录、背景音乐、音效、MP3 音乐库、限时奖励、关卡系统、虚拟摇杆、数据导出导入与离线游玩。每个账号可自定义头像和昵称、选择电脑/手机设备，数据完全独立。无需安装任何依赖，双击即可游玩。

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
| v7.2.0 | 当前最新版：登录/注册页一键添加到主屏幕 | https://aaaaaaaalh.github.io/hungry-snake/versions/v7.2.0/ |
| v7.1.0 | 数据导出导入 + 注册合并游客战绩 + PWA 离线 + 安全区适配 | https://aaaaaaaalh.github.io/hungry-snake/versions/v7.1.0/ |
| v7.0.1 | 修复 200 分无法进入关卡 3 | https://aaaaaaaalh.github.io/hungry-snake/versions/v7.0.1/ |
| v7.0.0 | 关卡 3 + 地图随关卡变大 + 关卡彩蛋 | https://aaaaaaaalh.github.io/hungry-snake/versions/v7.0.0/ |
| v6.2.0 | 手机端界面瘦身 + 操作提示可关闭 + 修复吃苹果突然死亡 | https://aaaaaaaalh.github.io/hungry-snake/versions/v6.2.0/ |
| v6.1.1 | 右上角按钮与音量控件放大 2 倍 | https://aaaaaaaalh.github.io/hungry-snake/versions/v6.1.1/ |
| v6.1.0 | 右上角工具栏 + 游客可查历史账号 + 放大操作提示 | https://aaaaaaaalh.github.io/hungry-snake/versions/v6.1.0/ |
| v6.0.0 | 音量滑杆 + 关卡系统 + 账号战绩列表 | https://aaaaaaaalh.github.io/hungry-snake/versions/v6.0.0/ |
| v5.0.0 | 限时奖励 + 虚拟摇杆 + 设备选择 | https://aaaaaaaalh.github.io/hungry-snake/versions/v5.0.0/ |
| v4.0.1 | 修复音乐库面板打不开的问题 | https://aaaaaaaalh.github.io/hungry-snake/versions/v4.0.1/ |
| v4.0.0 | MP3 音乐库（公共库 + 私人库） | https://aaaaaaaalh.github.io/hungry-snake/versions/v4.0.0/ |
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
3. 查看历史账号 / 战绩：点击右上角「用户档案」按钮（未登录也能看）
4. 登录 / 注册 / 切换账号：点击右上角「登录 / 注册」按钮
5. 调节音量：拖动右下角音量滑杆（拖到 0 即静音）
6. 自定义音乐：点击右上角「🎵 音乐库」，上传 MP3 到公共库或私人库并选用
7. 关卡系统：达到 100 分可选择进入关卡 2，左下角会出现墙，撞墙即死
8. 备份 / 恢复：右上角「用户档案」→「数据管理」→ 导出数据 / 导入数据，换设备也能带走账号与音乐库
