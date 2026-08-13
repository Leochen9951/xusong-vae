# 许嵩 · 成名之路 🎵

苹果官网设计风格的单页网站，讲述许嵩（Vae）从网络歌手到时代唱作人的成名之路。内置 Apple Music 风格的悬浮循环播放器。

## ✨ 功能特性

- 🎨 苹果官网设计风格（毛玻璃导航、大标题排版、滚动动画）
- 🎵 悬浮音乐播放器：上一首 / 播放暂停 / 下一首 / 静音 / 进度拖拽
- 🔁 三种循环模式：列表循环、单曲循环、随机播放
- ⌨️ 键盘快捷键：`空格` 播放/暂停，`←` / `→` 切歌
- 📱 响应式设计，手机端同样流畅

## 🎶 添加歌曲（重要）

许嵩的音乐作品受版权保护，**请使用你自己合法拥有的音频文件**（如购买的正版数字音乐），将文件放入 `audio/` 文件夹，文件名与 `index.html` 中 `PLAYLIST` 配置一致：

| 歌曲 | 文件名 |
|------|--------|
| 素颜 | `audio/suyan.mp3` |
| 有何不可 | `audio/youhebukeyi.mp3` |
| 灰色头像 | `audio/huisetouxiang.mp3` |
| 千百度 | `audio/qianbaidu.mp3` |
| 断桥残雪 | `audio/duanqiaocanxue.mp3` |
| 雅俗共赏 | `audio/yasugongshang.mp3` |
| 乌鸦 | `audio/wuya.mp3` |

> 支持 `.mp3` / `.m4a` / `.ogg` 等格式；想增删歌曲，直接编辑 `index.html` 里的 `PLAYLIST` 数组即可。
> 注意：GitHub 单文件上限 100MB，建议单曲不超过 25MB（可先用 128kbps 压缩）。

## 🚀 部署到 GitHub Pages

### 方法一：网页操作（推荐新手）

1. 打开 [github.com/new](https://github.com/new)，仓库名填 `xusong-vae`（或其他名字），**不要**勾选 "Add a README file"，点 Create repository
2. 在本项目目录打开终端，执行：

```bash
git remote add origin https://github.com/<你的用户名>/xusong-vae.git
git branch -M main
git push -u origin main
```

3. 回到 GitHub 仓库页面 → **Settings** → 左侧 **Pages** → Source 选择 **Deploy from a branch** → Branch 选 **main**、目录选 **/(root)** → Save
4. 等 1~2 分钟，访问：

```
https://<你的用户名>.github.io/xusong-vae/
```

### 方法二：GitHub CLI（一步到位）

```bash
gh repo create xusong-vae --public --source . --push
```

创建后在仓库 Settings → Pages 里开启 Deploy from branch 即可（同上第 3 步）。

## 📁 项目结构

```
xusong-vae/
├── index.html      # 主页面（含全部样式与播放器）
├── audio/          # 存放歌曲文件
└── README.md       # 本说明
```

## ⚠️ 版权声明

本页面为设计演示，文字内容仅供学习参考；许嵩的音乐作品版权归许嵩及所属唱片公司所有，请勿在公网传播未经授权的音频文件。
