# 许嵩 · 成名之路 🎵

苹果官网设计风格的单页网站，讲述许嵩（Vae）从网络歌手到时代唱作人的成名之路。内置「音乐馆」专区：**官方 MV 在线播放 + 官方平台直达链接**。

## ✨ 功能特性

- 🎨 苹果官网设计风格（毛玻璃导航、大标题排版、滚动动画）
- 🎬 **官方 MV 专区**：5 支来自许嵩本人与所属厂牌（太合音乐）官方账号的 MV，Bilibili 官方播放器在线播放
- 🎵 **单曲直达**：其余单曲为 VIP 付费曲目，提供网易云音乐 / QQ 音乐官方页面链接
- 📱 响应式设计，手机端同样流畅
- 🌐 不存储、不传播任何音频/视频文件，完全合规

## 🎬 官方 MV（已实测可嵌入）

| MV | B站视频号 | 来源账号 |
|----|----------|---------|
| 乌鸦 | BV1H64y127hM | 许嵩官方（mid=647208864） |
| 老古董 | BV1WU4y1a7sW | 太合音乐（mid=37791459） |
| 如约而至 | BV1sb4y1Q74g | 太合音乐 |
| 装糊涂 | BV1yy4y187SF | 太合音乐 |
| 弹指一挥间 | BV1Yp4y1h7LU | 太合音乐 |

**增删 MV**：编辑 `index.html` 中的 `MVS` 数组（bvid 为 B 站视频号）。
> 只建议收录**官方账号**（许嵩官方 / 太合音乐）发布的视频；粉丝搬运的视频内容本身侵权且随时可能被下架。

## 🎶 关于单曲（为什么是"链接"而不是"播放器"）

许嵩的歌曲在网易云、QQ 音乐等平台均为 **VIP 付费曲目**，平台禁止 VIP 歌曲外链播放（已实测：播放地址接口返回为空）。
因此公网版本无法在网页内直接播放单曲，改为提供官方页面链接，点击后跳转到平台收听。

**增删单曲**：编辑 `index.html` 中的 `SONGS` 数组：

```js
const SONGS = [
  { title: '素颜', album: '寻雾启示', netease: 167827, qq: '004Gq0xE1YC8xp' },
  // ...
];
```

- `netease`：网易云歌曲 ID（网页版地址 `music.163.com/#/song?id=XXXX` 中的数字）
- `qq`：QQ 音乐 songmid（`y.qq.com/n/ryqq/songDetail/XXXX` 末尾的字符串）

## 💻 本地测试版（可选）

如需本地循环播放原唱（**仅供个人使用，勿上传公网**），工作区根目录有 `xusong-vae.html`（本地测试版），
将你付费下载的歌曲文件放入其同级的 `audio/` 文件夹即可用悬浮播放器循环播放（同样含官方 MV 专区）。

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
├── index.html      # 主页面 V1（Apple 风格：含 MV 专区、音乐馆与动画）
├── v2/
│   └── index.html  # 设计体验版 V2（编辑杂志风：明暗主题、跑马灯、大色块）
├── v3/
│   └── index.html  # 进化版 V3（三主题色切换：墨绿/靛蓝/粉 + 动效升级）
└── README.md       # 本说明
```

- V2 访问地址：`https://<你的用户名>.github.io/xusong-vae/v2/`
- V3 访问地址：`https://<你的用户名>.github.io/xusong-vae/v3/`

## ⚠️ 版权声明

本页面为设计演示，文字内容仅供学习参考；音乐与 MV 由 Bilibili / 网易云音乐 / QQ 音乐官方提供，版权归许嵩及所属唱片公司所有。
