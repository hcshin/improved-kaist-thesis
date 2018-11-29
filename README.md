IMPROVED KAIST Thesis Format in LaTeX
=====================================

With the original version of KAIST thesis format (Dissertation Template.zip, https://www.kaist.ac.kr/html/kr/edu/edu_03030309.html), one can choose between "draft" and "final" mode in the original version of KAIST thesis format (defiend by kaist-ucs.cls). However, the draft mode in the original format is quite impractical, because:
* It does not display any images. Images are replaced by boxes and filenames in draft mode.
* Even in draft mode, it prints too much unncessary information: table of contents, table of tables, table, of figures, acknowledgement, CV, etc.

With above problems solved, the draft mode can be conveniently used for producing handout document for thesis proposals and defenses. I fixed these problems, and in addition, improved following features:
* The original format does not support BibTeX, which is widely used for generating bibliography in LaTeX documents. IMPROVED KAIST Thesis Format supports BibTeX.
* When compiled, the original format generates multiple LaTeX fontsize warnings due to adoption of unsupported fontsizes. These warnings are fixed in IMPROVED KAIST Thesis Format.
* In the original format, all contents are included in a single file (sample_in_English.tex). IMPROVED KAIST Thesis Format has distributed contents files which are located in *sections/*.

## Features
* Using "draft" mode, a concise handout document for thesis prorposals and defenses can be generated.
    * Images are well displayed even in draft mode.
    * Unnecessary information for handout documents (table of contents, table of tables, table, of figures, acknowledgement, CV, etc.) are ommited in draft mode.
* Added BibTeX support.
* Distributed contents into multiple *.tex files.
* No compilation warnings in the original format.

## How to Use
Compile main.tex as usual.
* To compile in draft mode: in "main.tex", comment out the line with "\finaltrue" and make the line with "\finalfalse" take effet.
* To compile in final mode: in "main.tex", comment out the line with "\finalflase" and make the line with "\finaltrue" take effet.
 
## Compilation Test Info.
Compilation tested in/with:
* Ubuntu 16.04
* vim-latex + texlive-full package (pdfTeX 3.14159265-2.6-1.40.16, BibTex 0.99d)
