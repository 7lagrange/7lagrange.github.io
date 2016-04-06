---
layout: post
title: "ipython-table-style"
date: 2016-04-06
---


use the style in pandas
```
#https://github.com/HHammond/PrettyPandas
#http://melissagymrek.com/python/2014/01/12/ipython-tables.html
#http://nbviewer.jupyter.org/gist/chris1610/f2f4a2e9181f6ec22e88
#http://nbviewer.jupyter.org/github/pydata/pandas/blob/master/doc/source/html-styling.ipynb

def color_negative_red(val):
    """
    Takes a scalar and returns a string with
    the css property `'color: red'` for negative
    strings, black otherwise.
    """
    color = 'red' if val < 0.05 else 'black'
    return 'color: %s' % color

df = pd.DataFrame(np.array([[1,2,0.03],[0.1,0.001,0.00001]]), index=('aaa','bbb'),columns=('lib', 'qty1', 'qty2'))

styles = [
    dict(selector="th:not(empty)", props=[("font-size", "100%"),("text-align", "center"),('background-color','#FFEBCD'),
                              ('border','1px solid white')]),
    dict(selector="td", props=[("background-color", "#f4f4ff"),('border','1px solid #ccf'),("text-align", "center"),
                              ('padding','0.5em'),('border','2px solid #ccf')]),
    dict(selector="tr", props=[('border','none')]),
    dict( props=[('font-size','200%'), ('font-family','Helvetica'),('border-collapse','collapse'),('border','none')
                ])
]
s = df.style.applymap(color_negative_red,subset=pd.IndexSlice[:, ['lib', 'qty2']]).set_table_styles(styles)
s

```
