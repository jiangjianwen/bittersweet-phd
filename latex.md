**Table of Contents:**

[TOC]

# Latex Packages & Tricks

Things could make your writing easier and your paper more professional.

[Overleaf](https://www.overleaf.com) is a convenient online collaborative latex writing platform. It also provides some basic latex writing tips [here](https://www.overleaf.com/learn/latex).

<!-- ## Misc. -->


## Control float environments
- [A comprehensive answer!](https://tex.stackexchange.com/questions/39017/how-to-influence-the-position-of-float-environments-like-figure-and-table-in-lat)
  - Some parameters in the above document could be very helpful
  - e.g. put `\setlength{\textfloatsep}{5pt plus 1pt minus 1pt}`(default 20pt plus 2pt minus 4pt) before `\begin{document}`, this would **_save a lot of space between top or bottom tables/figures and the text area_**
- Options `b` and `h` are disabled for `table*` and `figure*` environments (cross-column tables and figures)


## [_**"subcaption"**_](https://ctan.org/pkg/subcaption?lang=en): Create sub-figures and sub-tables

- [Sub-figures](https://www.overleaf.com/learn/latex/How_to_Write_a_Thesis_in_LaTeX_(Part_3):_Figures,_Subfigures_and_Tables#Subfigures)

<img src=https://cdn.sharelatex.com/learn-scripts/images/5/58/Thesisthree.png width=400/>

- [Sub-tables](https://www.overleaf.com/learn/latex/How_to_Write_a_Thesis_in_LaTeX_(Part_3):_Figures,_Subfigures_and_Tables#Subtables)

<img src=https://cdn.sharelatex.com/learn-scripts/images/d/dc/Thesistwo.png width=400/>

- [Official document](http://ctan.math.utah.edu/ctan/tex-archive/macros/latex/contrib/caption/subcaption.pdf)

<!-- ## Lists -->

## [_**"enumitem"**_](https://ctan.org/pkg/enumitem?lang=en): Control layout of itemize, enumerate & description

_"enumitem"_ is a very helpful package if you want to reduce spaces in itemize/enumerate environments

- A simple example:

import the package first: `\usepackage{enumitem}` then put
`\setlist{nosep,after=\vspace{0.5\baselineskip},leftmargin=12pt}` before before `\begin{document}`, this would (globally) remove separations between items, reduce the space at the bottom of list environments and reduce the left indentation to 12pt.

- [More examples](https://tex.stackexchange.com/questions/184780/can-someone-please-explain-the-enumitem-horizontal-spacing-parameters)
- [Official document](http://ctan.math.washington.edu/tex-archive/macros/latex/contrib/enumitem/enumitem.pdf)




<!-- ## Tables -->


## [_**"booktabs"**_](https://ctan.org/pkg/booktabs?lang=en): Beautiful tables
<img src=https://i.stack.imgur.com/qSvmi.png width=200/>

_"booktabs"_ might be one of the most popular latex packages in academic writing.

- [A simple example](https://www.latex-tutorial.com/tutorials/tables/#Booktabs)
  - _personal preference: vertical lines are ugly here, don't use them._
- [A fancier example (stepped table)](https://tex.stackexchange.com/questions/433930/stepped-table-in-booktabs?rq=1)
- [Another fancy example (with multi-columns)](https://tex.stackexchange.com/questions/163061/help-with-a-booktabs-table)
- [Official document](http://ctan.math.utah.edu/ctan/tex-archive/macros/latex/contrib/booktabs/booktabs.pdf)

## [_**"makecell"**_](https://ctan.org/pkg/makecell?lang=en): Force line breaks inside a table cell
This package can be very helpful if you want to force line breaks inside a table cell

- [Examples](https://tex.stackexchange.com/questions/2441/how-to-add-a-forced-line-break-inside-a-table-cell/45069)
- [Official document](http://ftp.math.purdue.edu/mirrors/ctan.org/macros/latex/contrib/makecell/makecell.pdf)

## [_**"tabularx"**_](https://ctan.org/pkg/tabularx?lang=en): Tabulars with adjustable-width columns

- [Examples](https://en.wikibooks.org/wiki/LaTeX/Tables#The_tabularx_package)
- [Official document](http://mirrors.concertpass.com/tex-archive/macros/latex/required/tools/tabularx.pdf)


<!-- ## Figures -->

<!-- ## Math -->

## Quotation Marks and Dashes
- ***Single quotation marks: ` and '***
- ***Double quotation marks: `` and ''***
- Even fancier [examples](https://en.wikibooks.org/wiki/LaTeX/Text_Formatting#Quote-marks)
- [Dashes](https://en.wikibooks.org/wiki/LaTeX/Text_Formatting#Dashes_and_hyphens): 
  - - inter-word
  - -- page range, 1–10
  - --- punctuation dash
  - `$-$` minus sign

## Resize parentheses, brackets and braces 
- [Resize automatically](https://www.overleaf.com/learn/latex/Brackets_and_Parentheses#Introduction)
  - simple `\left(` and `\right)` would work in most cases
- [Resize manually](https://www.overleaf.com/learn/latex/Brackets_and_Parentheses#Controlling_types_and_sizes)

## Overbrace and underbrace
- [A simple example](https://en.wikibooks.org/wiki/LaTeX/Advanced_Mathematics#Above_and_below): 

```
\[
 z = \overbrace{
   \underbrace{x}_\text{real} + i
   \underbrace{y}_\text{imaginary}
  }^\text{complex number}
\]
```
<img src=https://wikimedia.org/api/rest_v1/media/math/render/svg/19fb76203b478da82fe7475dd4f8fbedada1673b width=150/>

- [A fancier example (with overlaps)](https://tex.stackexchange.com/questions/297/how-can-i-get-an-underbrace-and-an-overbrace-to-partially-overlap-in-an-equation):  
  - [_**"underoverlap"**_](https://ctan.org/pkg/underoverlap?lang=en): a package to handle this case

## Math symbols and fonts
- [Greek letters and math symbols](https://www.overleaf.com/learn/latex/List_of_Greek_letters_and_math_symbols)
- [Mathematical Fonts](https://www.overleaf.com/learn/latex/Mathematical_fonts)
- `\mathit{}` could be useful for long identifiers in math

## [_**"bm"**_](https://ctan.org/pkg/bm): A lazy solution to bold symbols in maths mode
- [Official document](http://mirrors.concertpass.com/tex-archive/macros/latex/required/tools/bm.pdf)

## [_**"mathtools"**_](https://ctan.org/pkg/mathtools?lang=en): Beautiful maths
- [Examples](https://www.overleaf.com/learn/latex/Articles/Mathtools_-_for_beautiful_math)
- one of the most useful command might be `\mathclap{}`, which can reduce spaces in subscripts, exponents, etc.
- [Official document](http://mirrors.concertpass.com/tex-archive/macros/latex/contrib/mathtools/mathtools.pdf)


<!-- ## References -->

## [_**"cleveref"**_](https://ctan.org/pkg/cleveref?lang=en): A clever way to reference

_"cleveref"_ can help us to define unified reference formats in the global environment, so that we can keep using `\cref{}` regardless of the specific reference types (equation, section, etc.) in the document.

- [Examples](https://texblog.org/2013/05/06/cleveref-a-clever-way-to-reference-in-latex/)
- [Official document](http://ctan.math.washington.edu/tex-archive/macros/latex/contrib/cleveref/cleveref.pdf)


## [_**"xcolor"**_](https://ctan.org/pkg/xcolor?lang=en): Color your LaTex

- [Examples](https://www.overleaf.com/learn/latex/Using_colours_in_LaTeX)
- [Official document](http://ctan.math.illinois.edu/macros/latex/contrib/xcolor/xcolor.pdf)

