# my-docs

基于 **MkDocs + Material** 的技术文档站，通过 **GitHub Actions** 自动部署到 **GitHub Pages**。

## 在线地址

部署成功后可访问：`https://<你的GitHub用户名>.github.io/my-docs/`

## 目录结构

```
my-docs/
├── docs/                       # 存放 Markdown 文档（必填）
│   ├── index.md                # 主页（必填）
│   ├── about.md                # 关于页面（必填）
│   ├── guide.md                # 使用指南（必填）
│   └── api.md                  # API 参考（必填）
├── .github/
│   └── workflows/
│       └── deploy.yml          # 自动化部署工作流配置（必填）
├── mkdocs.yml                  # MkDocs 配置文件（必填）
└── README.md                   # 项目说明（可选）
```

## 本地预览

```bash
pip install mkdocs-material
mkdocs serve            # http://127.0.0.1:8000
mkdocs build            # 产物输出到 site/
```

## 部署流程

1. 创建 `gh-pages` 分支（Settings → Branches，从 main 创建，内容可为空）。
2. Settings → Actions → General → Workflow permissions，选择 **Read and write permissions** 并保存。
3. `git add . && git commit -m "初始化MkDocs项目并配置GitHub Actions" && git push origin main`
4. 工作流执行完成后，在 Settings → Pages 确认 Source 为 `gh-pages` 分支。
5. 等待 1–2 分钟后访问站点地址。
