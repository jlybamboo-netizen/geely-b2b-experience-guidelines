# GitHub Pages 部署说明

项目已包含 GitHub Pages 的纯静态构建与自动部署配置。

## 自动部署

1. 在 GitHub 新建仓库，并将项目推送到 `main` 分支。
2. 打开仓库的 **Settings → Pages**。
3. 在 **Build and deployment → Source** 中选择 **GitHub Actions**。
4. 打开 **Actions**，等待 `Deploy GitHub Pages` 完成。
5. Pages 页面会显示公开访问地址，通常为：
   `https://<账号名>.github.io/<仓库名>/`

以后每次更新并推送到 `main`，网站都会自动重新发布。

## 本地生成静态文件

```bash
pnpm install
pnpm run build:github-pages
```

生成结果位于 `github-pages-dist/`。该目录可以直接上传到 GitHub Pages、公司静态服务器、对象存储或任意静态托管平台。
