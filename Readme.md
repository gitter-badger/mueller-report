# mueller-report

The 2019 Mueller Report as an open LaTeX document.

- [Volume I: Russian Interference](https://github.com/iandennismiller/mueller-report/blob/master/products/mueller-report-vol-1.pdf)

## Motivation

The version of the Mueller Report distributed on April 18, 2019 suffers from several technical limitations.  This project is an effort to correct those limitations.

## Features

- full-text search
- high fidelity text; not deteriorated by photocopy, redaction, and optical character recognition
- split document into Vol 1 and Vol 2
- descriptive page header
- table of contents with working hyperlinks
- redactions can be represented explicitly in the source code
- canonical URL with greater permanence than DOJ distribution

## LaTeX Conventions

- each sentence in the source code is on its own line
- each top-level section is in a separate file using `\include`
- some symbols must be escaped with backslash: `%`, `#`, `@`, `$`, `&`, and `_`
- `\P` indicates a legal paragraph symbol
- `\S` indicates a legal section symbol
- `\hr` creates a horizontal rule
- `\xblackout{lorem ipsum}` creates a black box around some words
- `\footnote{lorem ipsum}` creates a footnote, which must start on its own line
    - the previous line must end with `%` to prevent newline
    - after the comment, the footnote number is noted; e.g. `% 63`
- `\textit{lorem ipsum}` creates italics
- `\textbf{lorem ipsum}` creates italics
- `\section{lorem ipsum}` is the top-level heading
- `\subsection{lorem ipsum}` is the second-level heading
- `\subsubsection{lorem ipsum}` is the third-level heading
- `\begin{quote}` indicates a block quote
- `\begin{enumerate}[i]` produces a list with lowercase roman numerals
    - `\item` is an individual list item

## Redacting template

The following text is an example for how redacted text will be represented in the working document.  It is expected that once ongoing matters have resolved, this document will become progressively unredacted.

    \xblackout{Harm to Ongoing Matter: Lorem ipsum dolor sit amet, consectetur
        adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
        magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation
        ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute
        irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
        fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident,
        sunt in culpa qui officia deserunt mollit anim id est laborum.
    }

    \xblackout{Harm to Ongoing Matter: Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.}

## See also

- [Special Counsel's Office](https://www.justice.gov/sco)
- [2019-04-18 Mueller Report, Redacted](https://www.justice.gov/storage/report.pdf)
- [LaTeX censor package](https://ctan.org/pkg/censor)

## Todo

- smart quotes
- match outline glyphs (I, A, 1, a)
- footnotes, beginning with #33 on page 20.
- image on p. 31
- 
