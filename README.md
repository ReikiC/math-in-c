# Math in C

用 C 学习数学，从数学理解到代码编写一步到位。

## 本地开发

需要 [Docker](https://www.docker.com/) 和 [Docker Compose](https://docs.docker.com/compose/)。

```bash
docker compose up --build
```

打开 http://localhost:8888/lab/tree/work 即可编辑笔记。

- Markdown 单元格写公式（LaTeX 语法）
- Code 单元格写 C 代码，Shift+Enter 直接编译运行
- 改个数值重新运行，立刻看到结果

## Quarto 渲染

需要 [Quarto](https://quarto.org/)。

```bash
quarto render        # 输出到 _site/
quarto preview       # 本地预览
```

## GitHub Pages

推送到 `main` 分支后，GitHub Actions 自动渲染并发布。在仓库 Settings → Pages 中将 Source 设为 GitHub Actions 即可。

## 项目结构

```
notebooks/           # Jupyter 笔记本（.ipynb）
├── 01-basics.ipynb
docker-compose.yml   # 本地开发环境
_quarto.yml          # Quarto 配置
```