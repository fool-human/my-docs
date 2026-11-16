# API 参考

这里是 API 参考文档示例。

## 站点配置项

| 配置项 | 位置 | 说明 |
| ------ | ---- | ---- |
| `site_name` | `mkdocs.yml` | 网站名称，显示在页面标题和导航栏 |
| `theme.name` | `mkdocs.yml` | 主题名，`material` 为 Material 主题 |
| `nav` | `mkdocs.yml` | 导航结构，对应 `docs/` 下的文件 |

## 部署工作流参数

```yaml
on:
  push:
    branches: [main]
    paths: ['docs/**', 'mkdocs.yml']
```
