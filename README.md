# Math in C

用 C 学习数学 — 在 Jupyter 里写公式、跑代码，Quarto 自动渲染成带输出结果的笔记网站。

## 本地开发

```bash
docker compose up --build
```

启动后同时运行两个服务：

| 服务 | 地址 | 用途 |
|------|------|------|
| Jupyter Lab | http://localhost:8888 | 写笔记、跑 C 代码 |
| Quarto Preview | http://localhost:4444 | 实时预览渲染后的网站 |

工作流：在 Jupyter (8888) 中编辑 notebook，保存后 Quarto (4444) 自动热重载，浏览器刷新即可看到最新渲染结果。

## 在线阅读

推送到 `main` 分支后，GitHub Actions 自动将 `_site/` 部署到 GitHub Pages。

## 技术栈

- **Jupyter + C Kernel** — Markdown 单元格写 LaTeX 公式，Code 单元格写 C 代码并直接运行
- **Quarto** — 将 notebook 渲染为静态网站
- **Docker Compose** — 一键启动完整开发环境
- **GitHub Pages** — 自动部署

## 添加新章节

1. 在 `notebooks/` 下新建 `.ipynb` 文件
2. 在 `_quarto.yml` 的 `chapters` 中添加对应路径
3. Jupyter 中编辑并运行，Quarto 自动预览
