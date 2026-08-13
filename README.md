# 许嵩 · 成名之路 🎵

苹果官网设计风格的单页网站，讲述许嵩（Vae）从网络歌手到时代唱作人的成名之路。内置「音乐馆」专区，提供**网易云音乐 / QQ 音乐官方页面直达链接**。

## ✨ 功能特性

- 🎨 苹果官网设计风格（毛玻璃导航、大标题排版、滚动动画）
- 🎵 音乐馆专区：7 首代表作的**官方平台直达按钮**（网易云 + QQ 音乐）
- 📱 响应式设计，手机端同样流畅
- 🌐 不存储、不传播任何音频文件，完全合规

## 🎶 关于音乐（为什么是"链接"而不是"播放器"）

许嵩的歌曲在网易云、QQ 音乐等平台均为 **VIP 付费曲目**，平台禁止 VIP 歌曲外链播放（已实测：播放地址接口返回为空）。
因此公网版本无法在网页内直接播放原唱，改为提供官方页面链接，点击后跳转到平台收听（登录自己的账号即可）。

**增删歌曲**：编辑 `index.html` 中的 `SONGS` 数组：

```js
const SONGS = [
  { title: '素颜', album: '寻雾启示', netease: 167827, qq: '004Gq0xE1YC8xp' },
  // ...
];
```

- `netease`：网易云歌曲 ID（网页版地址 `music.163.com/#/song?id=XXXX` 中的数字）
- `qq`：QQ 音乐 songmid（QQ 音乐网页版歌曲链接 `y.qq.com/n/ryqq/songDetail/XXXX` 中末尾的字符串）

## 💻 本地测试版（可选）

如需本地循环播放原唱（**仅供个人使用，勿上传公网**），工作区根目录有 `xusong-vae.html`（本地测试版），
将你付费下载的歌曲文件放入其同级的 `audio/` 文件夹即可用悬浮播放器循环播放。

## 🚀 部署到 GitHub Pages

### 方法一：网页操作（推荐新手）

1. 打开 [github.com/new](https://github.com/new)，仓库名填 `xusong-vae`，**不要**勾选 "Add a README file"，点 Create repository
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

本页面为设计演示，文字内容仅供学习参考；音乐链接指向网易云音乐 / QQ 音乐官方页面，版权归许嵩及所属唱片公司所有。
