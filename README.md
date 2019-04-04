# ThiThesisTemp

A simple beautiful LaTeX theme for books, thesis.

- Author: [DINH Anh-Thi](http://dinhanhthi.com "Thi's personal website").
- This template is modified (a lot) from [The Legrand Orange Book](https://www.latextemplates.com/template/the-legrand-orange-book) which is also a modifed version of other works.
- This theme borrows the basic structure of TLOB but it wears a new suit which is lighter and simpler.

## Features

1. Indexes.
2. Glossaries.
3. Table of content on each chapter.
4. Algorithms.
5. Flexibly inserting images.
6. Boxed math equations.
7. Boxes for theorem, definition,... environments.
8. Beautiful table theme.
9. Classify references into different types (books, thesis, articles)
10. Back link to pages for the bibliography.

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

## Centering headings/titles

In the case you don't like the title of thesis, chapters which are floating to the right and you want them to be at the center. Just do, 

- Copy & Overwrite files **center_headings/cover.tex** and **center_headings/cover-eng.tex** the files in the root folder. 
- Copy and Overwrite file **center_headings/chapter-heading.tex** to the file in **/settings**.

Be careful, after overwriting, all contents you modified in the *cover.tex* and *cover-eng.tex* will disappear. If you have already modified these files, just compare two files and manually replace the settings lines.