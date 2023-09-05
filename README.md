# BMC_Dissertation_Template
BMC_Dissertation_Template

Bryn Mawr College dissertation LaTeX template. The template is designed to work within Overleaf projects.

The overleaf [link](https://www.overleaf.com/read/tdmvhyzkkrch)

The titlepage:
[titlepage.tex](titlepage.tex)

The template:
[template.tex](template.tex)

The package:
[bmctemplate.sty](bmctemplate.sty)

The package uses the following packages: 
- hyperref, 
- url, 
- [utf8] inputenc, 
- import, 
- [titlesec](https://ctan.org/pkg/titlesec?lang=en), 
- [titletoc](https://ctan.org/pkg/titlesec?lang=en), 
- setspace, 
- xparse, 
- [document] ragged3e, 
- [a4paper, left=1.5in, right=1in, top=1in, bottom=1in] geometry,
- xcolor, 
- indentfirst
- caption
- subcaption
- [biblatex](https://ctan.org/pkg/biblatex)

---
The template sets many of the LaTeX environments to match the BMC dissertation requirements: chapter/section headings, table of contents, appendicies, titlepage, abstract, acknowledgement, etc.

The **bmc_template** package contains two options:
- double
- bibconfig

The BMC dissertations are required to be double spaced. The **double** option changes the linespacing to double space. Keeping the double space as an option allows the content creator to toggle between single spacing and double spacing to their liking during the editing stages of their dissertation.

The bibliography is required to have each bibitem with a hanging indent and single spaced. Spacing between bibitems must be double spaced. The **bibconfig** option incorporates a basic implementation of the format. However, to incorporate your preferred citation method and the bibliographic requirements you will have to code the bibliography latex environment yourself. The titlepage package documentation includes information on how to change the bibliography environment.


# Bibliography Setup
[issue #7](https://github.com/cacsphysics/BMC_Dissertation_Template/issues/7) describes an alternative way to properly format the bibliography. 

The bibliography setup currently used within the template was constructed with various stackexchange information. The solutions within [the link](https://tex.stackexchange.com/questions/400644/no-hanging-indent-with-biblatex-in-bibliography) are very helpful. In addition, the [biblatex package](https://ctan.org/pkg/biblatex) was curcial in understanding the **\defbibenvironment{}** biblatex command.

The Bibliography code block:
```
{
\RequirePackage[
        backend=biber,
        style=phys,
        biblabel=brackets,
        articletitle=true
    ]{biblatex}
    \defbibenvironment{bibliography}
        {\list{\printtext[labelnumberwidth]{%
            \printfield{labelprefix}%
            \printfield{labelnumber}}}
        {\setlength{\leftmargin}{\bibhang}%
            \setlength{\itemindent}{-\leftmargin}%
            \setlength{\itemsep}{2\baselineskip plus .05\baselineskip minus .05\baselineskip}%
            \setlength{\parsep}{\bibparsep}}
        }
        {\endlist}
    {\item}
}
```

# Table of Contents Setup
The table of contents (titletoc), and chapter, section and subsection headers, are formatted using the [titlesec packages](https://ctan.org/pkg/titlesec?lang=en), there are three. 
> I wish the author of the titlesec manual used the hyperref package.


