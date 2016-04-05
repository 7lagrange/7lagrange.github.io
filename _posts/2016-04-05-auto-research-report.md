---
layout: post
title: "Automatically generating research report"
date: 2016-04-05
---


There are many advatanges of automatically generating report when doing research. 
If we have a small change of the input, it will be convenient to have all the downstream analysis in one script.
The report will be reproducible and error free.

I found two ways to do it.

## R markdown 
R markdown use [knitr](http://yihui.name/knitr/) and embedded R code to generate PDF, simply click the Knit PDF button. 
Bascially it generates md files and convert to pdf, it requires knitr, pandoc, latex



## Ipython notebook

we can use ipython notebook to do computing and visualization interactively and convert the results to pdf or slides.

1.Ipython notebook

   You can do the analysis in ipython notebook and view the results in 
	have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown)  
	To have a line break without a paragraph, you will need to use two trailing spaces

    1. German Shepherd
    2. Belgian Shepherd
        1. Malinois
        2. Groenendael
        3. Tervuren
2. Cat
    1. Siberian
    2. Siamese


1. Ipython notebook



2. Ipython notebook convert to slides
⋅⋅* Unordered sub-list.
3. Ipython notebook convert to pdf
⋅⋅⋅To have a line break without a paragraph, you will need to use two trailing spaces.⋅⋅
⋅⋅⋅Note that this line is separate, but within the same paragraph.⋅⋅

``` bash

/usr/local/bin/pandoc +RTS -K512m -RTS Example_Ipython.md --to beamer --from markdown+autolink_bare_uris+ascii_identifiers+tex_math_single_backslash-implicit_figures --output wgs.call.compare.20160112.revised.pdf --highlight-style tango --latex-engine /Library/TeX/texbin/pdflatex

```

