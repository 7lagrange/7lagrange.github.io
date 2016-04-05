---
layout: post
title: "Automatic research report"
date: 2016-04-05
---


There are many advatanges of automatically generating report when doing research. 
If we have a small change of the input, it will be convenient to have all the downstream analysis in one script.

I found two ways to do it.

## R markdown 
R markdown use [knitr](http://yihui.name/knitr/) and embedded R code to generate PDF, simily click the Knit PDF button. 
Bascially it generates md files and convert to pdf, it requires knitr, pandoc, latex

``` bash

/usr/local/bin/pandoc +RTS -K512m -RTS Example_Ipython.md --to beamer --from markdown+autolink_bare_uris+ascii_identifiers+tex_math_single_backslash-implicit_figures --output wgs.call.compare.20160112.revised.pdf --highlight-style tango --latex-engine /Library/TeX/texbin/pdflatex

```
## Ipython notebook

we can use ipython notebook to do computing and visualization interactively and convert the results to pdf or slides.

1. First ordered list item
2. Another item
⋅⋅* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
⋅⋅1. Ordered sub-list
4. And another item.

⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅
⋅⋅⋅(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses


1. Ipython notebook

⋅⋅⋅You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅
⋅⋅⋅(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

2. Ipython notebook convert to slides
⋅⋅* Unordered sub-list.
3. Ipython notebook convert to pdf
⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅

