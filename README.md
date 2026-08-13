# 许嵩 · 成名之路 🎵

苹果官网设计风格的单页网站，讲述许嵩（Vae）从网络歌手到时代唱作人的成名之路。内置「音乐馆」专区，通过**网易云音乐官方播放器**在线听歌。

## ✨ 功能特性

- 🎨 苹果官网设计风格（毛玻璃导航、大标题排版、滚动动画）
- 🎵 音乐馆专区：7 首代表作的网易云**官方正版播放器**，边读边听
- 📱 响应式设计，手机端同样流畅
- 🌐 无任何音频文件存储，完全合法，不怕版权投诉

## 🎶 关于音乐（重要）

- 页面不存储、不传播任何音频文件
- 歌曲通过网易云音乐官方外链播放器（iframe）从官方服务器播放
- 版权归许嵩及原权利人所有，本站仅作展示

**增删歌曲**：编辑 `index.html` 中的 `SONGS` 数组：

```js
const SONGS = [
  { id: 167827,     title: '素颜',     album: '寻雾启示' },
  // ...
];
```

获取歌曲 ID：网易云网页版打开歌曲 → 地址栏 `music.163.com/#/song?id=XXXX` 中的数字即 ID。

> ⚠️ 若某首歌显示「版权受限/无法播放」，说明该曲未开放外链，换一首或删除该条目即可。

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
├── index.html      # 主页面（含全部样式、音乐馆与动画）
└── README.md       # 本说明
```

## ⚠️ 版权声明

本页面为设计演示，文字内容仅供学习参考；音乐由网易云音乐官方播放器提供，版权归许嵩及所属唱片公司所有。
