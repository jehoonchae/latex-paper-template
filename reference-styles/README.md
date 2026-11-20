# Reference presets

Select one preset with `\input{reference-styles/NAME}` in `preamble.tex`.
Change `\input{reference-styles/apsr}` to the desired preset and save. The manuscript body and its
combined SI remain the same for every choice. The two example references
exercise a book and a three-author journal article.

## What each preset implements

- **APSR:** uses the supplied `apsr-natbib.bst`, including
  its existing typography. It is a modified historical APSR/Harvard style,
  not a new implementation of every current Chicago rule.
- **APA 7:** uses `biblatex-apa` (`style=apa`) with Biber and American English.
  This implements seventh-edition references; `apacite` is not used because
  its APA implementation is sixth edition. Keep complete author names and
  DOI fields in the database; the style supplies initials and DOI formatting.
- **AJPS, JOP, POQ:** share `biblatex-chicago` author-date with full given
  names and `dashed=false`, so repeated authors are written out. The
  installed package implements Chicago 17; AJPS and POQ now refer to
  Chicago 18. These are working Chicago-based presets, with final house-style
  details to be checked against the linked journal instructions. Changing
  the package version may change edge cases in reference formatting.
- **JASA:** uses Brett Presnell's contributed `asa.bst` (1998), for the
  **American Statistical Association**. It supplies initialed author names,
  parenthesized years, quoted article titles, and author-year citations.
  This is a legacy style, not the Acoustical Society's JASA style or the
  American Sociological Association's style. It does not print DOI/URL fields.
  `longnamesfirst` prints full author lists on the first citation; for six or
  more authors, add `\shortcites{key1,key2}` after `\begin{document}` to use
  the short form from the outset. Order multiple keys chronologically to
  follow the ASA guide. The bundled style is unchanged; its original
  redistribution notice remains in the file.
- **JRSS B:** uses natbib with `abbrvnat`, the bibliography style in the
  optional OUP/RSS template currently linked by the Series B instructions.
  Those instructions allow any readable reference style at submission.
  The preset follows that submission template, rather than claiming to
  reproduce the journal's final typeset reference list.

The reference options do not apply journal submission layouts, blinding,
word limits, or journal-specific appendix requirements. They preserve the
template fonts, margins, title pages, statement spacing, and combined SI.

## Sources checked on November 20, 2026

- [APSR author instructions](https://www.cambridge.org/core/journals/american-political-science-review/information/author-instructions/preparing-your-materials)
- [biblatex-apa, APA 7 support](https://ctan.org/pkg/biblatex-apa)
- [biblatex-chicago](https://ctan.org/pkg/biblatex-chicago)
- [AJPS manuscript preparation](https://ajps.org/guidelines-for-manuscripts/manuscript-preparation/)
- [JOP style guide](https://www.journals.uchicago.edu/journals/jop/style)
- [POQ general instructions](https://academic.oup.com/poq/pages/general_instructions)
- [Taylor & Francis ASA reference guide](https://files.taylorandfrancis.com/tf_R.pdf)
- [Source of the bundled ASA style](https://raw.githubusercontent.com/cran/CSFA/master/vignettes/asa.bst)
- [JRSS B author instructions](https://academic.oup.com/jrsssb/pages/general-instructions)
- [OUP/RSS template linked by JRSS B](https://www.overleaf.com/latex/templates/template-for-journal-of-the-royal-statistical-society-series-c-applied-statistics/xhkktkrcfswc)

The standard packages `natbib`, `biblatex-apa`, `biblatex-chicago`, `babel`,
and `csquotes`, plus `abbrvnat.bst`, come from the LaTeX installation. Only the
supplied APSR style and the contributed ASA style need to travel with this
folder. Keep both supplied `.bst` files with their original notices.
