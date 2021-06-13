---
title: LaTeX
---

A configuration and initialization file for LatexMk

```perl
$clean_ext = "sta";
$clean_full_ext = "sta";

# $aux_dir = "output.output";
# $out_dir = "output.output";

$pdf_mode = 1; # tex -> pdf

# If no files are specified, latexmk will, by default, run on all files in the current working directory with a ".tex" extension.
# If you have your work split up into several parts, you have to specify the main file like this
@default_files = ('main.tex');
# Or maybe you want to process several files
# @default_files = ('file-one.tex', 'file-two.tex');

# When the source file uses bbl files for bibliography, run bibtex or biber as needed to regenerate the bbl files.
$bibtex_use = 2;

$pdf_previewer = 'start "c:/Program Files/SumatraPDF/SumatraPDF.exe" %O %S';

$pdflatex = 'pdflatex -shell-escape %O %S';
```

Class file of academic CV.

```latex
% Telling the compiler which version of LaTeX the package is for
\NeedsTeXFormat{LaTeX2e}

% Giving the compiler some information about your package
% The first argument should match the filename of you class file
% The second argument is optional and provides a description of your class which will appear in the log and other places.
% The description must begin with a date in exactly the format and it should be the date the package was last modified.
% E.g. \documentclass{myCV}[2016/07/12] with a date which is newer than the date of last modification, a waring will be shown saying that the class is outdated.
\ProvidesClass{myCV}[2016/06/28 My custom CV class]

% Load all commands from "article" class
\LoadClass[12pt,a4paper]{article}

% Layout setup
\RequirePackage[top=2cm, bottom=2cm, outer=2cm, inner=5cm, heightrounded, marginparwidth=4cm, marginparsep=1cm]{geometry}

% Add notes to margin
\RequirePackage{marginnote}
\reversemarginpar % notes appear on the left

% Printing out page layout parameters
\RequirePackage{layout}
% \layout{}

% Font packages
% Setting section titles to bold and all capital with "\bfseries\scshape"
%\RequirePackage{libertine}
\RequirePackage{times}
%\RequirePackage{DejaVuSerif}
%\RequirePackage[T1]{fontenc}
% \usepackage{mathpazo}
% \usepackage{newtxtext}

% Access to Lorem ipsum context for testing
\RequirePackage{lipsum}
% \lipsum[1-10]

% Modifying the section title
% Include "titlesec" package to customize our header styles.
% "\RequriedPackage" rather than "\usepackage" is being used since we are in ".cls" file, and it makes sure that each package is only loaded once.
\RequirePackage{titlesec}

\titlespacing{\section}{0cm}{-1em}{0.1em}

% Section title customization
\titleformat
{\section} % command
[display] % shape
{\bfseries\scshape\raggedright\large} % format
{} % label
{0em} % sep
{
    % \rule{\textwidth}{1pt}
    % \vspace{1ex}
    % \centering
} % before-code
[
% \vspace{-0.5ex}%
% \rule{\textwidth}{0.3pt}
\titlerule
] % after-code

\titleformat
{\subsection}
[display]
{\raggedright}
{}
{0em}
{}
[]

\newcommand{\datedsubsection}[2]{%
	\subsection[#1]{#1 \hfill #2}%
}
```