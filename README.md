# Latex document definition

This repo contains the most common structures used in professional document writing with latex
It follows stypitic rules for bib references and the document itselfs as follows 

## Structure 

* preamble: contains all package and command definitions. Everything should be set by now, but if something needs defining this is the place to do it (look inside to see the structure)
* bibfiles
    * local.bib: contains all local bib references i.e., references used for this paper specifically. Most references should be added here
    * bib folder: this folder contains many references used for multiple purposes, in particular the _compsci.bib_ file contains many references on software engineering, programming languages, and adaptive systems. Check here if the reference exists before adding it to the _local.bib_ file
* acronym.tex: contains all Acronyms used in the paper (look into the file for example of the definition). Acronyms are used with the _\ac{ACRONYM}_ command


## Useful commands

* \comment[TYPE]{AUTHOR}{COMMENT} is used to leave annotation inlined with the text. Comments only appear in draft mode (the option in the documentclass in the _main.tex_ file) and are invisible otherwise. Type can be comment, missing, idea, author.
* Figures, theorems, tables, etc are to be referenced using the command \fref{}, which automatically generates the appropriate reference as Figure 1., Theorem 1., ..... according to the delimiter used (fig:, sec:, tab:, thm:, ln:, enum:, ....)
* _\ie \eg \cf_ are used respectively for the abbreviations i.e., e.g., cf.
* listings are defined according to each specific language in the _preamble_ file and generate their own environment (e.g., _\java[....]{....}_ generates a java listing).

## Style guidelines

* Citations should be prepended by a ~ and no space (e.g., word~\cite{ref1, ref2}). This ensures that the references are nicely separated and arranged when the bibtex engine is placing them in the document.
* Inlined lists (created using the \begin{enumerate*}[label=(\arabic*)] command) should be indexed with arabic numbers between parenthesis (1). This is easier to read and is a nice style [Dubpre 98. Bugs in writing].
* The paper should be written in **American** English.
