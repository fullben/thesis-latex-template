# Thesis Template

A bachelor's/master's thesis template based on the [thesis template](https://github.com/uniba-dsg/dsg-templates/tree/master/dsg-thesis-en) of the Distributed Systems Group of the University of Bamberg.

A compiled version of the template in its current state is provided in the [thesis.pdf](thesis.pdf) file.

## Structure

This section provides a brief introduction to the overall structure and major files of the template.

- [thesis.tex](thesis.tex): Main file, defines the overall structure of the document. Use this file to include the individual section/chapter files of your thesis.
- [misc/setup.tex](misc/setup.tex): The preamble of the template. Defines packages to be included and all custom commands.
- [bibliography/references.bib](bibliography/references.bib): The file for defining all the sources used as references in the thesis. You may also place any copies of the referenced works in this directory.
- [abbreviations/abbreviations.tex](abbreviations/abbreviations.tex): The file for defining all acronyms used.
- `figures`: Default directory for all figure files.
- `sections`: Default directory for the sections/chapter files.

## Noteworthy Features

This section outlines the most important features and commands of this template.

### Thesis Information Configuration

The template has various `\setXXX` commands, which can be used for configuration. Commands such as `\setthesistitle` can be utilized to define the title of the thesis. The template will use this title on the title page. Furthermore, most of the `\setXXX` commands have a matching `\XXX` command for printing the set value. Using `thesistitle` anywhere in the document will therefore result in the thesis title being printed.

All available set-commands are called and documented in the initial section of the [thesis.tex](thesis.tex) file. They can be used to customize the title page (university name, faculty name, title, author name, and so on) and the declaration of authorship.

Important commands:

- `\setdeclaration`: Can be used to define the contents of the *Declaration of Authorship* printed at the end of the thesis.
- `\setgroup`: Sets the name of research group or chair the thesis will be submitted to. Aside from being printed on the title page, the name of this group will also be included in the footer of all pages.

### Code Listing Styles and Environments

The template defines two custom styles and corresponding environments for code listings.

There is a style (`javaStyle`) and evironment (`javacode`) for Java, based on the IntelliJ IDEA Classic Light Theme, adjusted for red-green vision deficiency. This style defines additional delimiters and colors for highlighting annotations (e.g., `%%@Override%%`), numbers (e.g., `~~5~~`), and constants (e.g., `,,INIT_VALUE,,`).

A second style (`sqlStyle`) and environment (`sqlscript`) for highlighting SQL script segments is also provided.

### Including Figures

The template defines two commands for including figures:

- `\includefigure{label}{filename}{caption}{width}`: Insert a graphic wrapped in a figure environment. The graphic is expected to be found in the `figures` directory.
- `\includewrappedfigure{alignment}{width}{filename}{caption}{label}`: Insert a graphic wrapped in a figure environment, with text wrapping around the image. The graphic is expected to be found in the `figures` directory.
