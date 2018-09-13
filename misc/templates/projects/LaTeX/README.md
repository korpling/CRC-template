---
title: "How to use the LaTeX template"
author: felix.golcher@hu-berlin.de
header-includes:
- \usepackage{fullpage}
- \setmonofont[Contextuals=Alternate]{Junicode}
date: Wed Feb  7 21:02:53 CET 2018
---

# Files #

* **wrapper.tex**: Wrapper file containing the preamble and
  including P00.tex and P00.bib. If you need additional LaTeX
  packages, include here. Better don't change too much,
  otherwise the length of the document could change. But no change is
  taken directly to the final document so don't be scared.
* **P00.tex**: Text goes here. It should not exceed 3 pages. The
  assumed encoding is UTF-8.
* **P00.bib**: Bib(la)tex file. Bibliographic references go here. This
  file is supposed to be encoded in UTF-8. If edited by jabref, the
  program should recognize this automatically.

# Workflow #

Change **P00.tex** to your needs, add literature to **P00.bib** and necessary
packages to **project_description.tex** and compile **project_description.tex**.

The files are designed to work with XeTeX and biber.

Files are supposed to be encoded in UTF-8.

# misc #

## Project-related publications or other sub-bibliographies ##

If you want to have some references bundled into a sub-bibliography, put the respective citations into a \verb!\refsection!-environment as is shown in the following code example:

```
\begin{refsection}
\nocite{test1}
 \printbibliography[heading=subbibliography, title={~}]
\end{refsection}
```

## IPA ##

The following code may be used to set IPA-font.

```
{\fontspec{Junicode}
hwɑn θɑt ɑːprɪl wiθ is ʃuːrəs soːtə θə drʊxt ɔf mɑrʧ hɑθ peːrsəd toː
θə roːte ɑnd bɑːðəd ɛvrɪ væɪn ɪn swɪʧ lɪkuːr ɔf hwɪʧ vɛrtɪu
ɛnʤɛndrəd ɪs θə fluːr hwɑn zɛfɪrʊs eːk wɪθ hɪs sweːtə bræːθ
}
```
This is only one of the possibilities for including IPA.

# Help #

[Felix Golcher (felix.golcher@hu-berlin.de)](mailto:felix.golcher@hu-berlin.de)

