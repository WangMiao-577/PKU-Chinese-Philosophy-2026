# 中国哲学（上）

2026–2027 学年个人学习归档 · Simson。

中国哲学概述、先秦诸子、礼乐文明、孔子、墨子与老子。讨论课按第一轮“礼”和第二轮“老子”分别归档，阅读材料、个人讨论笔记和参考书互相独立。

GitHub 公开仓库：[PKU-Chinese-Philosophy-2026](https://github.com/WangMiao-577/PKU-Chinese-Philosophy-2026)。每个课程目录有自己的独立 Git 历史。

## 从哪里开始

- [课堂笔记源码](Notes/Chinese%20Philosophy.tex)
- [课堂笔记 PDF](Notes/Chinese%20Philosophy.pdf)
- [资料索引](FILE_INDEX.md)

## 目录

- `Notes/`：课堂笔记、主 LaTeX 文件、章节源码、插图与已有 PDF。
- `Slides/`：课程课件和课堂演示资料。
- `Discussions/`：讨论课题目、阅读材料、讨论笔记与分轮参考书。
- `Archives/`：旧编译文件、旧编辑器配置或暂未分类资料。
- `LargeFiles/`：大文件分卷与 SHA-256 校验清单。
- `tools/`：分卷还原工具。

## 本地编译

与三个主目录的布局配套时，在本课程根目录运行：

```bash
python3 "../../latex/build.py" "Notes/Chinese Philosophy.tex"
```

编译脚本会切换到主文件所在目录，使用工作区已有 MiKTeX/XeLaTeX，并关闭缺包自动安装。源码引用的章节和图片均保持在对应 Notes 目录内。单独获取此课程仓库时，可用自己已有的 XeLaTeX 在 Notes 中编译；中文与代码字体使用本机已有字体。

## 大文件

本地完整文件保持可直接阅读。GitHub 中以 32 MiB 分卷存储，不需要 Git LFS 或其他新软件。在仓库根目录执行：

```bash
python3 tools/restore_large_files.py
python3 tools/restore_large_files.py --verify
```

还原器先核对各分卷 SHA-256，再按原目录还原完整文件。已存在但校验不一致的文件不会被覆盖。大文件包括：

- `Discussions/Round1-Ritual/References/三礼通论-钱玄.pdf`（234.5 MiB，8 卷）
- `Discussions/Round1-Ritual/References/春秋左传注-杨伯峻.pdf`（71.6 MiB，3 卷）
- `Discussions/Round1-Ritual/References/礼记译解-王文锦.pdf`（209.1 MiB，7 卷）
- `Discussions/Round2-Laozi/References/北京大学藏西汉竹书（贰）.pdf`（119.5 MiB，4 卷）

## 保存范围与来源

课程资料和已有学习结果完整保留。LaTeX 中间产物、依赖缓存与生成构建文件只在本地保存，不进入公开仓库。第三方材料保留原文件名、README、LICENSE 或版权说明；这些资料的权利属于原作者，本仓库不为它们追加统一开放许可证。内容仍以现有课堂记录为准，整理没有补写尚未完成的章节。
