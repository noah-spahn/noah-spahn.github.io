---
title: "Latex notes"
date: 2022-03-17T14:26:05-07:00
tags: []
draft: true
---

```sudo apt install texlive-latex-extra```

```sudo apt install texlive-science```

Then make a test document:

```sudo vim test.tex```

```\documentclass{article}
\usepackage{hyperref}
\begin{document}
Hello world \LaTeX

\url{https://linuxconfig.org}
\end{document}
```

then test the document:

`pdflatex test.tex`

and view it:

`evince test.pdf`


To make use of a specialized editor, install it!

`sudo apt install texstudio`

If you are running a minimal Ubuntu installation, there may still be a need to add a thesuarus. 


The simplest solution to this may just be downloading from the apt package: 

`sudo apt install mythes-en-us`


If you would like to have other language specific dictionary/thesaurus tooling, you will have to track
down a free one, perhaps this one [from
 apache](https://extensions.openoffice.org/en/project/english-dictionaries-apache-openoffice)
would work. Be sure to restart texstudio after you have made the changes.


Further details can be found in the documenation, which is (by default) placed
in `file:///usr/share/doc/texstudio/html/usermanual_en.html`. 

Fancy formatting options are available in other packages:

`sudo apt install texlive-publishers` and `sudo apt install texlive-pictures` might include what is needed.


