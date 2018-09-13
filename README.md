# CRC-template

LaTeX template for Collaborative Research Center proposals following
the DFG guidelines.

* Mainmaintainer: [Felix Golcher](https://github.com/felixgolcher)
* Collaborators: [Thomas McFadden](https://github.com/mcfadden13), [Thomas Krause](https://github.com/thomaskrause), [Anke Lüdeling] (https://github.com/AnkeLuedeling)

## Structure and Subdirs 

```
.
├── cv
├── figures
├── misc
│   ├── logos
│   ├── templates
│   │   ├── cv
│   │   │   ├── LaTeX
│   │   │   └── Word
│   │   └── projects
│   │       ├── LaTeX
│   │       └── Word
│   └── unpublished
└── projects
```

* `cv/`: Curricula Vitae
* `projects/`: Project descriptions
* `figures/`: additional figures, possibly provided by projects etc.
* `misc/`: logos are supposed to be from participating organizations. Templates are edited by coworkers.


## Files & Workflow

### Top level wrapper

* `Concept.tex`: Master LaTeX file.

### input files

* `preamble.tex`: Macro definitions. Outsourced to reduce code doubling in main wrappers.
* `includeonly.tex`: If this file exists, it is `\input`ed. It is not tracked by git. Every user can have a different one. If you include a line like `\includeonly{general}` in this file, only the file `general.tex` will be `\include`d.
* `cvlist.tex` List of CVs. For not having to change all wrappers at the same time if a new projects or the like is introduced
* `projectlist.tex`: Same for list of project descriptions.
* `general.tex`: general section
* `keydata.tex`: keydata section
* `collaborators.tex`: Summary list of collaborators.
* `fundingbreakup.tex`: See below for creation of this file.
* `mainfundingtable.tex`: See below for creation of this file.


### knitr, input and output ###

The following line of code can be used to produce the `\inputted` Textables from the spreadsheet and the knitr-Code:
```
Rscript -e 'library(knitr); knit("fundingbreakup.Rnw"); knit("mainfundingtable.Rnw")'
```

#### Additional Files ####

* `funding.ods`: Add all information about the cost structure here. Three sheets are used:
    1. `staff`: Which project will use what staff? This table is rather directly translated to Table 1.2 ("breakdown by subproject").
    2. `direct`: Direct costs. This sheet is rather directly used to produce the lower part of Table 1.1 ("Overview of requested funding").
    3. `costcat`: Which category of employment costs how much money per year? This information is used to produce the upper part of Table 1.1
* `fundingbreakup.Rnw`: Code to produce Table 1.2 ("breakdown by subproject")
* `fundingbreakup.tex`: Secondary file, produced by above mentioned Code snippet from `funding.ods` and `fundingbreakup.Rnw`.
* `mainfundingtable.Rnw`: Code to produce Table 1.1 ("Overview of requested funding").
* `mainfundingtable.tex`: Secondary file, produced by above mentioned Code snippet from `funding.ods` and `mainfunding.Rnw`.
* `Concept.bib`: bibliographic data base.




