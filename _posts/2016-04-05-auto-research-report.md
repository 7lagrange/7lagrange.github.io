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

we can use ipython to do computing and visualization interactively and convert the results to pdf or slides.

Results can be uploaded to github and viewed at [nbviewer](http://nbviewer.jupyter.org/)

- Ipython notebook

   use [Jupyter notebook extensions](https://github.com/ipython-contrib/IPython-notebook-extensions) to hide code cells and add table of contents  
   Hiding only works locally

- Ipython notebook convert to slidemarkdow

   [IPython notebook reveal-based slideshows](http://www.slideviper.oquanta.info/tutorial/slideshow_tutorial_slides.html#/)  

   ipython nbconvert mynotebook.ipynb --to slides --post serve    

      the command will generate a slide html in browser  
      [generate html slideshow](http://stackoverflow.com/questions/20441848/how-do-i-separate-slides-when-exporting-an-ipython-notebook-to-reveal-js)
      add --reveal-prefix reveal.js

   ipython nbconvert mynotebook.ipynb --to slides  --template output_toggle --post serve  

      * [Hide the input cells from your IPython slides](http://www.damian.oquanta.info/posts/hide-the-input-cells-from-your-ipython-slides.html) 
      [Hide notebook prompt](http://stackoverflow.com/questions/32358778/hide-ipython-notebook-prompt)  

- Ipython notebook convert to markdown/latex/pdf

``` 
command convert mb to pdf 

/usr/local/bin/pandoc +RTS -K512m -RTS Example_Ipython.md --to beamer --from markdown+autolink_bare_uris+ascii_identifiers+tex_math_single_backslash-implicit_figures --output wgs.call.compare.20160112.revised.pdf --highlight-style tango --latex-engine /Library/TeX/texbin/pdflatex

```

# Some useful links

