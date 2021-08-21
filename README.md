# Primary-Graphs
Graphs for the CICM and ANZCA primary exams written in latex. Includes:
* .tex
* .dvi
* .ps  
Contains files that `dvisvgm` couldn't convert from .dvi. Built using `dvips`, and converted with an online tool.
* .svg  
SVGs have been compiled from tex using [dvisvgm](dvisvgm.bplaced.net) and stripped of extraneous (and height+width data) using [SVGO](https://github.com/svg/svgo).

## How-To
(For my recollection)
* Make the tex files
* Run `latexmk -dvi` in the folder containing the .tex files
Requires Perl.
* Run 
`Get-ChildItem "*.dvi" |
    Foreach-Object {
       & dvisvgm "$($_.FullName)"  --font-format=woff
}` in the folder containing the .dvi files