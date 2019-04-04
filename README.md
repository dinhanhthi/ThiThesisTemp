# ThiThesisTemp

A simple beautiful LaTeX theme for books, thesis.

- Author: [DINH Anh-Thi](http://dinhanhthi.com "Thi's personal website").
- This template is modified (a lot) from [The Legrand Orange Book](https://www.latextemplates.com/template/the-legrand-orange-book) which is also a modifed version of other works.
- This theme borrows the basic structure of TLOB but it wears a new suit which is lighter and simpler.

## How to use this theme?

This theme is made for ones who love [texmaker](http://www.xm1math.net/texmaker/) and [texstudio](https://www.texstudio.org/). If you use other TeX editors and cannot compile this theme, please let me know at [dinhanhthi@gmail.com](mailto:dinhanhthi@gmail.com).

## How to compile?

On **Linux** or **MacOS**, use following commands for the first compilation.

~~~ bash
pdflatex -synctex=1 -interaction=nonstopmode main.tex; makeindex main.idx -s StyleInd.ist; makeglossaries -s main.ist main; biber main; pdflatex -synctex=1 -interaction=nonstopmode main.tex; pdflatex -synctex=1 -interaction=nonstopmode main.tex
~~~

On **Windows**, use following commands for the first compilation.

~~~ bash
pdflatex.exe -synctex=1 -interaction=nonstopmode main.tex && makeindex.exe main.idx -s StyleInd.ist && makeglossaries.exe -s main.ist main && biber.exe main && pdflatex.exe -synctex=1 -interaction=nonstopmode main.tex && pdflatex.exe -synctex=1 -interaction=nonstopmode main.tex
~~~

For both cases, if you have no more on the glossary and index (you only use the ones made from the first build), you can run only with **PdfLaTeX** and **biber** as other normal LaTeX document.
