---
layout: post
title: Twitterのアイコン生成
date: 2016-12-15
tags: blog LaTeX
---

ツイッターのアイコンを変えた。アイコンは某TeX藝人な方を真似てLaTeXで生成。pdflatexでPDFにして、画面をキャプチャして画像化（適当）した。正直LaTeXじゃなくても作れる。

{% highlight TeX %}
\documentclass{article}
\usepackage{graphicx,color}
\usepackage{fbb}
\begin{document}
\definecolor{kaihaku}{cmyk}{0,0.029,0.1,0.063}
\pagecolor{black}
\textcolor{kaihaku}{x}
\end{document}
{% endhighlight %}