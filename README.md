# A $\LaTeX$ Template for Academic Reseach Papers

This repository is a $\LaTeX$ template for academic research papers. It contains

1. Title page design.
2. Page style management.
3. Chapter files management.
4. Usages of common math symbols.
5. Usages of figures and tables.
6. Reference management.

## Table of Contents

- [Install](#install)
- [Usage](#usage)
  - [Directory Structure](#directory-structure)
  - [How to get the PDF file?](#how-to-get-the-pdf-file)
  - [Customize your information](#customize-your-information)
- [Maintainer](#maintainer)
- [License](#license)

## Install

This repository uses $\LaTeX$ and requires only the standard packages. To install $\LaTeX$, check out the installation process at [$\LaTeX$ project](https://www.latex-project.org/).

## Usage

### Directory Structure

```
LaTeX_template
|
|-------paper.tex (MAIN)
|
|-------attachment
|
|-------pgs
|       |
|       |-------protected
|       |       |
|       |       |-------newChpt.tex
|       |
|       |-------TitlePage.tex
|       |
|       |-------Confidential.tex
|       |
|       |-------CH_abstract.tex
|       |
|       |-------EN_abstract.tex
|       |
|       |-------contents.tex
|       |
|       |-------preface.tex
|       |
|       |-------chpt1.tex
|       |
|       |-------ref.tex
|       |
|       |-------attachment.tex
|       |
|       |-------Acknowledgement.tex
|
|-------pics
|       |
|       |-------protected
|               |
|               |-------logo_BNU.png
|
|-------res
        |
        |-------Preamble.sty
        |
        |-------ErrorInfo.md
        |
        |-------CommentInfo.md
        |
        |-------Preamble
                |
                |-------Article
                |       |
                |       |-------ArticleSettings.tex
                |       |
                |       |-------ContentsSettings.tex
                |       |
                |       |-------Fonts.tex
                |       |
                |       |-------Graphics.tex
                |       |
                |       |-------PageSettings.tex
                |       |
                |       |-------TableSettings.tex
                |       |
                |       |-------PagestyleDef.tex
                |       |
                |       |-------CodestyleDef.tex
                |       |
                |       |-------Article_NewCommand.tex
                |       |
                |       |-------Text_NewCommand.tex
                |
                |-------CHNSettings
                |       |
                |       |-------C_ChineseFonts.tex
                |       |
                |       |-------C_Math_TheoremEnvironment.tex
                |
                |-------Math
                |       |
                |       |-------Math_EnvironmentSettings.tex
                |       |
                |       |-------Math_Fonts.tex
                |       |
                |       |-------Math_Symbols.tex
                |       |
                |       |-------Math_TheoremEnvironment.tex
                |       |
                |       |-------Math_NewCommand.tex
                |
                |-------WarningSolver
                        |
                        |-------LaTeXFontWarningSolver.tex
```

### How to get the PDF file?

Compile `paper.tex` in `XeLaTeX` mode in TeXworks editor, [paper.pdf](LaTeX_template/paper.pdf) will be the result.

### Customize your information

1. To change **the logo of university**, 
    - Put the logo image file in `pics/protected/`. 
    - Go to pgs/[TitlePage.tex](LaTeX_template/pgs/TitlePage.tex). At line 13, 
    ```latex
    {\zihao{1}\includegraphics[width=0.5\linewidth]{protected/logo_BNU.png}}
    ```
    change `protected/logo_BNU.png` to the filename of the logo you just added. 
2. To change **the title of your paper**, go to [paper.tex](LaTeX_template/paper.tex). At line 9-14,
    ```latex
    % Enter the title here.
    \newcommand{\titlethesisCHN}{论文题目}
    \newcommand{\titlethesisENG}{TitleThesis}

    \newcommand{\titlethesisCHNi}{\titlethesisCHN}
    \newcommand{\titlethesisCHNii}{}
    ```
    change `论文题目` and `TitleThesis` to your title in CHN and ENG, respectively.
    Notice that `\titlethesisCHNi` and `\titlethesisCHNii` will be used in pgs/[TitlePage.tex](LaTeX_template/pgs/TitlePage.tex). If your title is longer than **28** characters, you should separate it into two lines.
3. To change **your personal info on the titlepage**, go to pgs/[TitlePage.tex](LaTeX_template/pgs/TitlePage.tex). At line 30-45,
    ```latex
    \textbf{\songti \makebox[59pt][l]{}部\quad\ 院\quad\ 系：\quad}
    \\[0.7em]
    \textbf{\songti \makebox[59pt][l]{}专\qquad\quad\ \ 业：\quad}
    \\[0.7em]
    \textbf{\songti \makebox[59pt][l]{}学\qquad\quad\ \ 号：\quad}
    \\[0.7em]
    \textbf{\songti \makebox[59pt][l]{}学\ \ 生\ \ 姓\ \ 名：\quad}
    \\[0.7em]
    \textbf{\songti \makebox[59pt][l]{}指\ \ 导\ \ 老\ \ 师：\quad}
    \\[0.7em]
    \textbf{\songti \makebox[59pt][l]{}指导教师职称：\quad}
    \\[0.7em]
    \textbf{\songti \makebox[59pt][l]{}指导教师单位：\quad}
    \\[3em]
    \begin{center}
    \textbf{\zihao{-4}\qquad\qquad\qquad 2023年\quad 月\quad 日}
    ```
    change the corresponding info to yours.

## Maintainer

[@Eicmlye](https://github.com/Eicmlye)

## License

[MIT](LICENSE) © Eric Monlye
