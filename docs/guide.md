# 使用指南

1. 编写 Markdown 文档
2. 提交代码到 GitHub
3. GitHub Actions 自动构建并部署

## 本地预览

```bash
pip install mkdocs-material
mkdocs serve
```

浏览器打开 <http://127.0.0.1:8000> 即可实时预览，修改 Markdown 后页面会自动刷新。

## 自动部署

向 `main` 分支推送 `docs/**` 或 `mkdocs.yml` 的改动时，
`.github/workflows/deploy.yml` 会依次执行：检出代码 → 设置 Python → 安装 MkDocs →
`mkdocs build` → 用 `JamesIves/github-pages-deploy-action` 把 `site/` 推到 `gh-pages` 分支。
