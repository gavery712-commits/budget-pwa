# 月度收支账本（PWA 版）

手机可安装、离线可用、支持 CSV 导出。本仓库用于 GitHub Pages 部署。

## 一、快速部署（无需 Actions）
1. 新建 GitHub 仓库（Public），将本仓库文件全部上传到 **main** 分支根目录。
2. 打开仓库 Settings → Pages：
   - **Build and deployment → Source** 选择 **Deploy from a branch**
   - **Branch** 选择 `main`，文件夹选择 `/ (root)`，保存。
3. 等待 GitHub Pages 完成构建，页面地址会显示在 Settings → Pages 顶部。

> 如果你更喜欢自动化部署，使用下面的 GitHub Actions 方式。

## 二、使用 GitHub Actions（推荐）
1. 保持本仓库结构不变，确保 `.github/workflows/pages.yml` 已存在。
2. 打开仓库 Settings → Pages：
   - **Build and deployment → Source** 选择 **GitHub Actions**。
3. 之后每次 push，都会自动部署到 Pages。

## 三、本地开发预览
直接用任何静态服务器（或浏览器直接打开 `index.html`）即可：

```bash
# Python 3
python -m http.server 5173

# 或者使用 node
npx serve .
```

访问 `http://localhost:5173`。

## 四、数据与隐私
记账数据保存在浏览器 `localStorage`（仅本机）。更换设备会丢失，请用“导出 CSV”定期备份。

## 五、图标 & PWA
- `manifest.webmanifest` 与 `service-worker.js` 已配置完毕
- iOS 可通过 Safari → 分享 → “添加到主屏幕”

祝使用愉快！