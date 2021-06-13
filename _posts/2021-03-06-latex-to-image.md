---
title: 用 LaTeX 画图
---

```latex
\documentclass[tikz,convert={outfile=\jobname.svg,convertexe={imgconvert.exe}}]{standalone}
%\usetikzlibrary{...}% tikz package already loaded by 'tikz' option
\begin{document}
\begin{tikzpicture}% Example:
  \draw (0,0) -- (10,10); % ...
  \draw (10,0) -- (0,10); % ...
  \node at (5,5) {Lorem ipsum at domine standalonus};
\end{tikzpicture}
\end{document}
```

使用 pdflatex 编译，会生成 pdf 和 svg。其中 svg 是由 pdf 转换而来，所以需要用到 ImageMagic 和 Ghostscrit。在 Windows 系统，最好把 convert.exe 重命名为 imgconvert.exe，避免和系统自带的 convert.exe 冲突。