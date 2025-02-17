# My Resume

I initially cloned this from some repo I found on the internet. The old README contents are on the section "# Old README" below

## Compile in Ubuntu 24.04

1. Install these packages: **texstudio, texlive-fonts-extra, texlive-bibtex-extra, biber, texlive-lang-portuguese** 
    - `sudo apt install texstudio texlive-fonts-extra texlive-bibtex-extra biber texlive-lang-portuguese`
    - Yes, these packages will require quite some space...
    - If you don't want to support more languages (as I do with Portuguese, omit the `texlive-lang-portuguese` package)

2. Open the file *main.tex* from this repo from the just installed *texstudio*
3. In **Options -> Configure TeXStudio... -> Build**:
    - **Default Compiler**: Use *PdfLaTeX*
    - **Commands**: Add the option "-shell-escape" to **PdfLaTeX**. My complete options look like this: `pdflatex -shell-escape -synctex=1 -interaction=nonstopmode %.tex` 
4. Compile it! (F6)

# Old Readme

It is based on AltaCV, from liantze@gmail.com

## AltaCV
Inspiration: [résumé of Marissa Mayer that Business Insider put together](http://www.businessinsider.my/a-sample-resume-for-marissa-mayer-2016-7/) using [enhancv.com](https://enhancv.com).

## Samples

This is how the re-created résumé looks like ([view/open on Overleaf](https://www.overleaf.com/read/gtqfpbwncfvp)):

Though if you're creating your own CV/résumé, you'd probably prefer using the basic template ([view/open on Overleaf](https://www.overleaf.com/read/trgqjpwnmtgv)):

## Requirements and Compilation

* pdflatex + biber + pdflatex
* AltaCV uses [`fontawesome`](http://www.ctan.org/pkg/fontawesome) and [`academicons`](http://www.ctan.org/pkg/academicons); they're included in both TeX Live 2016 and MikTeX 2.9.
* Loading `academicons` is optional: enable it by adding the `academicons` option to `\documentclass`.
* Can now be compiled with pdflatex, XeLaTeX and LuaLaTeX!
* However if you're using `academicons`, you _must_ use either XeLaTeX or LuaLaTeX. If the doc then compiles but the icons don't show up in the output PDF, try compiling with LuaLaTeX instead.
* The samples here use the [Lato](http://www.latofonts.com/lato-free-fonts/) font.
