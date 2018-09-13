---
title: "How to use the LaTeX template (cv)"
author: felix.golcher@hu-berlin.de
header-includes:
- \usepackage{fullpage}
date: Thu Mar 22 16:12:48 CET 2018
---

# Files #

* **wrapper.tex**: Wrapper file containing the preamble and including
  `MaxMustermann.tex` and `MaxMustermann.bib`. Changes to this
  document should not be necessary, except you want to change the name
  of the included files to match your name. It is not really necessary
  to send back this file.
* **MaxMustermann.tex**: Your cv goes here. Please use the suggested
  LaTeX-macros. The assumed encoding is UTF-8. There are German explanations in red. Those are from the DFG templates directly. They can be removed, but don't have to, since the responsible macro is deactivated centrally later.
* **MaxMustermann.bib**: Bib(la)tex file. Bibliographic references go here. This
  file is supposed to be encoded in UTF-8. If edited by jabref, the
  program should recognize this automatically.

# Workflow #

Change **MaxMustermann.tex** to your needs, add literature to
**MaxMustermann.bib** and compile **wrapper.tex**.

The files are designed to work with **xelatex** and biber. (In an earlier version instead of xelatex it said xetex. This was a lapse.)

If you want to change the name of the Mustermann files to match your
name, you have to adapt `wrapper.tex` to include those filles.

Files are supposed to be encoded in UTF-8.

# misc #

## Project-related publications or other sub-bibliographies ##

For the bibliographies special macros are provided.

