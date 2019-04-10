# ThiThesisTemp

A simple beautiful LaTeX theme for books, thesis. 

- **Demo**: file [main.pdf](https://github.com/dinhanhthi/ThiThesisTemp/blob/master/main.pdf) in the repository.
- **Author**: [DINH Anh-Thi](http://dinhanhthi.com "Thi's personal website").
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
11. Cover & Back cover. 
12. Multi languages.

## How to use this theme?

You can build this theme just by terminal at the first compilation. After that, you can build it by normal PdfLaTeX (in TeXStudio/TeXMaker or other TeX editors). If you have any trouble in compiling, please let me know at [dinhanhthi@gmail.com](mailto:dinhanhthi@gmail.com).

- Add new chapters
	- Add new files in **chapters/new-chapter.tex**. Just copy the example file **chap-example.tex**.
	- Don't foget to include them in the main file with `\subfile{chapters/new-chapter}`.
- Font matters are stored in **frontmatter/**.
- All new figures are stored in **figures/**. You don't need to include *figures/* in the path of the files. For example, if you have *figures/folder1/figure1.png*, you just use `\includegraphics{folder1/figure1}` in the file tex.

### Settings

- If you wanna make some **self-defined commands, environments**, add and modify them in file **settings/abbreviate-math.tex**.
- If you wanna modify the styles of **theorem boxes**, edit file **settings/theorem-style.tex**.
- If you wanna add more **glossaries**, edit file **settings/glossaries.tex**. **Importance:** After adding some new glossary, you *have to* run again command `makeglossaries -s main.ist main` besides other normal commands. For the ease, you compile the theme like the first time with command lines.
- If you wanna add some new **indexes**, you *have to* run again command `makeindex main.idx -s StyleInd.ist`.
- If you wanna use other colors rather than the blue as I give you as a default, check the file **settings/table-figure.tex**, step to lines which define color `tblue`. Keep the name **tblue** but use different RBG color. You can check the RBG code of some color [here](https://www.w3schools.com/colors/colors_rgb.asp).
- Other settings
	- Bibliography & Index: *settings/bib-index.tex*.
	- Fonts: *settings/font.tex*.
	- Hyperlinks: *settings/hyperlink.tex*.
	- Table of content: *settings/toc.tex*.
	- Table of content at the beginning of each chapter: *settings/mini-toc.tex*.
	- General packages: *settings/packages.tex*.
	- Header & Footer: *settings/page-header.tex*.
	- Headings: *settings/part-heading.tex*.
	- Margin of section: *settings/sec-numbering-margin.tex*.
	- Tables & Figures: *settings/table-figure.tex*.


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

- Copy & Overwrite files **center_headings/cover.tex** and **center_headings/cover-eng.tex** to the files who have the same name in the root folder. 
- Copy & Overwrite file **center_headings/chapter-heading.tex** to the file who has the same name in **settings/**.

Be careful, after overwriting, all contents you modified in the *cover.tex* and *cover-eng.tex* will disappear. If you have already modified these files, just compare two files and manually replace the settings lines.