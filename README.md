# BMC_Dissertation_Template
BMC_Dissertation_Template

Bryn Mawr College dissertation LaTeX template. The template is designed to work within Overleaf projects.

The overleaf [link](https://www.overleaf.com/read/tdmvhyzkkrch)

The titlepage:
[titlepage.tex](https://github.com/cacsphysics/BMC_Dissertation_Template/blob/main/titlepage.tex)

The template:
[template.tex](https://github.com/cacsphysics/BMC_Dissertation_Template/blob/main/template.tex)

The package:
[bmctemplate.sty](https://github.com/cacsphysics/BMC_Dissertation_Template/blob/main/bmctemplate.sty)

The package uses the following packages: 
- hyperref, 
- url, 
- [utf8] inputenc, 
- import, 
- titlesec, 
- titletoc, 
- setspace, 
- xparse, 
- [document] ragged3e, 
- [a4paper, left=1.5in, right=1in, top=1in, bottom=1in] geometry,
- xcolor, 
- indentfirst
- caption
- subcaption

---
The template sets many of the LaTeX environments to match the BMC dissertation requirements: chapter/section headings, table of contents, appendicies, titlepage, abstract, acknowledgement, etc.

The **bmc_template** package contains two options:
- double
- bibconfig

The BMC dissertations are required to be double spaced. The **double** option changes the linespacing to double space. Keeping the double space as an option allows the content creator to toggle between single spacing and double spacing to their liking during the editing stages of their dissertation.

The bibliography is required to have each bibitem with a hanging indent and single spaced. Spacing between bibitems must be double spaced. The **bibconfig** option incorporates a basic implementation of the format. However, to incorporate your preferred citation method and the bibliographic requirements you will have to code the bibliography latex environment yourself. The titlepage package documentation includes information on how to change the bibliography environment.

