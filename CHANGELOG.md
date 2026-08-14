# 更新日志

本项目所有版本变更都会记录在此文件，格式遵循 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/)，版本号遵循 [语义化版本](https://semver.org/lang/zh-CN/)（主版本.次版本.修订号）。

## [v1.0.0] - 2026-08-14

初始版本：贪吃蛇游戏上线。

### 新增
- 经典 20×20 网格贪吃蛇玩法，方向键 / WASD 控制方向
- 得分系统：每吃一个食物 +10 分，速度随得分逐渐加快
- 最高分本地保存（localStorage），刷新页面不丢失
- 暂停 / 继续（空格键）、重新开始（R 键 / 按钮）
- 手机触屏滑动控制
- 切换标签页自动暂停，防止误死
- GitHub Actions 工作流，push 后自动部署到 GitHub Pages
