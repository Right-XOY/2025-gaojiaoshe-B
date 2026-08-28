# 2025 高教社杯 B 题 · 碳化硅外延层厚度的确定

2025 年高教社杯全国大学生数学建模竞赛 B 题论文项目。基于 `cumcmthesis.cls` 国赛模板编写，使用 XeLaTeX 编译。

## 题目背景

碳化硅（SiC）是第三代半导体材料的代表。外延层厚度是外延材料的关键参数，对器件性能有重要影响。本项目利用**红外干涉法**，根据红外光谱的波长、外延层折射率和红外光入射角等参数，建立确定外延层厚度的数学模型，并对实测光谱数据（附件 1~4）进行求解与可靠性分析。

## 项目结构

```
.
├── article.tex            # 论文主文件（正文）
├── structure.tex          # 宏包与自定义环境（信息框、问题框、公式批注等）
├── cumcmthesis.cls        # 国赛模板类
├── .latexmkrc             # latexmk 配置（强制 xelatex，产物输出至 out/）
├── background/
│   ├── B题.md             # 赛题原文
│   └── 参考论文.md         # 参考文献整理
└── code/
    ├── q1.m               # 问题一求解（MATLAB）
    └── q2.py              # 问题二求解（Python）
```

## 编译方法

要求 XeLaTeX（模板对 `xeCJK` 有依赖），推荐通过 `.latexmkrc` 一键编译：

```bash
latexmk article.tex
```

或直接使用 XeLaTeX：

```bash
xelatex -synctex=1 -interaction=nonstopmode article.tex
```

> 编译产物统一输出到 `out/` 目录，已被 `.gitignore` 忽略。最终 PDF 为 `article.pdf`。

## 环境依赖

- TeX Live / MiKTeX（含 `ctex`、`xeCJK`、`mdframed`、`annotate-equations` 等宏包）
- 中文字体：项目根目录下 `YaHei.Consolas.1.11b.ttf` 与 `Fira Code Retina Nerd Font Complete.otf`（模板编译所需，请一并保留）

## 注意事项

- 提交前请替换 [article.tex](article.tex) 中的参赛编号（当前为占位 `123456`）与论文标题。
- 第 26~35 行为"华数杯"所属类别表格，国赛提交请整段注释或删除。
- 正文为通用模板结构（问题重述、问题分析、模型假设、符号说明、建模求解、灵敏度分析等），请按 B 题内容填充。
- 禁止公开真实参赛编号与论文数据；上传前请确认 `background/` 与正文中不含涉密/涉身份信息。

## License

本仓库仅供学习交流，请遵守全国大学生数学建模竞赛的参赛与论文规范。
