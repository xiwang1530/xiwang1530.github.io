# Xi Wang — 个人学术主页

一个自包含的静态网站（纯 HTML + CSS，无需任何编译/构建工具），用于展示你的个人简历、研究方向、论文、项目、荣誉与教学经历。

## 📁 文件夹结构

```
site/
├── index.html              ← 网页主文件（所有内容都在这里）
├── README.md               ← 本说明文件
└── assets/
    ├── profile.jpg         ← 你的头像照片
    └── Xi_Wang_CV.pdf       ← 可下载的 CV（"Download CV" 按钮指向它）
```

## 👀 先本地预览（不需要任何账号）

直接**双击 `index.html`**，它会在浏览器里打开。这就是网站最终的样子。改完内容后刷新即可看到效果。

---

## 🚀 发布到 GitHub Pages（让别人能访问）

GitHub Pages 是 GitHub 提供的**免费网页托管**。发布后，你的主页网址会是 `https://你的用户名.github.io`。

### 第 1 步：注册 GitHub 账号（免费，约 2 分钟）
打开 https://github.com → Sign up → 设置用户名（**这个用户名就是你的网址**，建议用 `xiwang`、`xi-wang-robotics` 之类专业一点的）。

### 第 2 步：新建仓库
- 登录后点右上角 **+ → New repository**
- **Repository name** 必须填成：`你的用户名.github.io`（例如用户名是 `xiwang`，就填 `xiwang.github.io`）
- 选择 **Public**
- 点 **Create repository**

### 第 3 步：上传网站文件
- 在仓库页面点 **Add file → Upload files**
- 把 `site/` 文件夹里的**全部内容**（`index.html`、`README.md` 和 `assets` 文件夹）拖进去
  - ⚠️ 注意：要上传的是文件夹**里面**的东西，让 `index.html` 位于仓库根目录，而不是套一层 `site/`
- 下方点 **Commit changes**

### 第 4 步：开启 Pages
- 进入仓库的 **Settings → Pages**
- **Source** 选 `Deploy from a branch`，Branch 选 `main` / 文件夹选 `/ (root)`，**Save**
- 等 1–2 分钟，刷新该页面，顶部会出现你的网址：`https://你的用户名.github.io`

完成 🎉 把这个网址发给别人即可。

---

## ✏️ 如何修改内容

所有内容都在 **`index.html`** 里，用任意文本编辑器（记事本、VS Code 等）打开即可。每个板块都有清晰的注释，例如：

- `<!-- ====== NEWS ====== -->` 动态板块
- `<!-- ====== SELECTED PUBLICATIONS ====== -->` 精选论文
- `<!-- ====== PROJECTS ====== -->` 项目与基金

改完保存、刷新浏览器即可。

### 换头像
把你的新照片命名为 `profile.jpg`，覆盖 `profile.jpg`（建议竖版、3:4 比例、宽度 ≥ 600px）。

### 换 CV
把你的新 CV 命名为 `Xi_Wang_CV.pdf`，覆盖 `Xi_Wang_CV.pdf`。

### 添加 LinkedIn / ORCID / Twitter 等链接
在 `index.html` 中找到 `<div class="quicklinks">`，仿照里面的 `<a>` 写法新增一行，例如：

```html
<a href="https://www.linkedin.com/in/你的ID" target="_blank" rel="noopener">
  <svg viewBox="0 0 24 24" fill="currentColor"><path d="M4 4h4v16H4zM10 9h4v2a4 4 0 0 1 7 3v6h-4v-5a2 2 0 0 0-4 0v5h-4z"/></svg>
  LinkedIn</a>
```

### 改主题色
在 `<style>` 顶部的 `:root{ }` 里改 `--accent`（主色）和 `--accent-d`（深色），全站颜色会自动跟着变。

---

## 说明
- 论文外链目前只接入了已确认的 Nature Communications 与一篇 arXiv 预印本。其余论文如有正式链接（DOI / IEEE Xplore / arXiv），可按精选论文卡片里 `<div class="links">` 的写法补上。
- 部分数据（如经费节省金额、媒体报道）来自你的 RAEng EOI 与 CV，发布前可再核对措辞。
