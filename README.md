# SYSU Beamer 模板

一个简洁的中山大学课程汇报 Beamer 模板。魔改自 THU-Beamer。

## 文件说明

- `main.tex`：主文档与示例内容
- `sysu.sty`：主题样式（配色、页脚、目录页等）
- `ref.bib`：文献数据库（BibTeX）
- `pic/`：图片资源目录

## 快速编译

推荐使用 XeLaTeX + BibTeX：

```bash
xelatex -interaction=nonstopmode main.tex
bibtex main
xelatex -interaction=nonstopmode main.tex
xelatex -interaction=nonstopmode main.tex
```

## 如何使用文献引用

1. 在 `ref.bib` 中新增条目（如 `@article{key,...}`）。
2. 在正文中用 `\cite{key}` 引用。
3. 文末使用：

```tex
\bibliographystyle{plain}
\bibliography{ref}
```

## 常见修改入口

- 改主题色与页脚：编辑 `sysu.sty`
- 改标题页信息：编辑 `main.tex` 的 `\title`、`\author`、`\institute`
