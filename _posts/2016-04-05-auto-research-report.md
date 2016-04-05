---
layout: post
title: "Auto research report"
date: 2016-04-05
---


There are many advatanges of automatically generating report when doing research. 
If we have a small change of the input, it will be convenient to have all the downstream analysis in one script.

I found two ways to do it.

# R markdown 
R markdown is can use knitir and emmbeded R code to generate PDF. bascially it generates md files and convert to pdf
/usr/local/bin/pandoc +RTS -K512m -RTS Example_Ipython.md --to beamer --from markdown+autolink_bare_uris+ascii_identifiers+tex_math_single_backslash-implicit_figures --output wgs.call.compare.20160112.revised.pdf --highlight-style tango --latex-engine /Library/TeX/texbin/pdflatex
