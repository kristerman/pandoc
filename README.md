<!-- Do not edit this file.  It is generated automatically from
README.template and MANUAL.txt via the command:
pandoc --lua-filter tools/update-readme.lua README.template -o README.md
-->
Pandoc
======

[![github release][]][] [![hackage release][]][] [![homebrew][]][]
[![stackage LTS package][]][] [![travis build status][]][] [![appveyor
build status][]][] [![license][]][] [![pandoc-discuss on google groups]]

  [github release]: https://img.shields.io/github/release/jgm/pandoc.svg?label=current+release
  [![github release][]]: https://github.com/jgm/pandoc/releases
  [hackage release]: https://img.shields.io/hackage/v/pandoc.svg?label=hackage
  [![hackage release][]]: http://hackage.haskell.org/package/pandoc
  [homebrew]: https://img.shields.io/homebrew/v/pandoc.svg
  [![homebrew][]]: http://brewformulas.org/Pandoc
  [stackage LTS package]: http://stackage.org/package/pandoc/badge/lts
  [![stackage LTS package][]]: http://stackage.org/lts/package/pandoc
  [travis build status]: https://img.shields.io/travis/jgm/pandoc/master.svg?label=travis+build
  [![travis build status][]]: https://travis-ci.org/jgm/pandoc
  [appveyor build status]: https://ci.appveyor.com/api/projects/status/nvqs4ct090igjiqc?svg=true
  [![appveyor build status][]]: https://ci.appveyor.com/project/jgm/pandoc
  [license]: https://img.shields.io/badge/license-GPLv2+-lightgray.svg
  [![license][]]: https://www.gnu.org/licenses/gpl.html
  [pandoc-discuss on google groups]: https://img.shields.io/badge/pandoc-discuss-red.svg?style=social
  [![pandoc-discuss on google groups]]: https://groups.google.com/forum/#!forum/pandoc-discuss

The universal markup converter
------------------------------

::: {#description}
Pandoc is a [Haskell] library for converting from one markup format to
another, and a command-line tool that uses this library.

Pandoc can read [Markdown], [CommonMark], [PHP Markdown Extra],
[GitHub-Flavored Markdown], [MultiMarkdown], and (subsets of) [Textile],
[reStructuredText], [HTML], [LaTeX], [MediaWiki markup], [TWiki markup],
[TikiWiki markup], [Creole 1.0], [Haddock markup], [OPML], [Emacs Org
mode], [DocBook], [JATS], [Muse], [txt2tags], [Vimwiki], [EPUB], [ODT],
and [Word docx].

Pandoc can write plain text, [Markdown], [CommonMark], [PHP Markdown
Extra], [GitHub-Flavored Markdown], [MultiMarkdown], [reStructuredText],
[XHTML], [HTML5], [LaTeX] (including [`beamer`] slide shows), [ConTeXt],
[RTF], [OPML], [DocBook], [JATS], [OpenDocument], [ODT], [Word docx],
[GNU Texinfo], [MediaWiki markup], [DokuWiki markup], [ZimWiki markup],
[Haddock markup], [EPUB] (v2 or v3), [FictionBook2], [Textile], [groff
man], [groff ms], [Emacs Org mode], [AsciiDoc], [InDesign ICML], [TEI
Simple], [Muse], [PowerPoint] slide shows and [Slidy], [Slideous],
[DZSlides], [reveal.js] or [S5] HTML slide shows. It can also produce
[PDF] output on systems where LaTeX, ConTeXt, `pdfroff`, `wkhtmltopdf`,
`prince`, or `weasyprint` is installed.

Pandoc's enhanced version of Markdown includes syntax for tables,
definition lists, metadata blocks, `Div` blocks, footnotes and
citations, embedded LaTeX (including math), Markdown inside HTML block
elements, and much more. These enhancements, described further under
Pandoc's Markdown, can be disabled using the `markdown_strict` format.

Pandoc has a modular design: it consists of a set of readers, which
parse text in a given format and produce a native representation of the
document (like an *abstract syntax tree* or AST), and a set of writers,
which convert this native representation into a target format. Thus,
adding an input or output format requires only adding a reader or
writer. Users can also run custom [pandoc filters] to modify the
intermediate AST.

Because pandoc's intermediate representation of a document is less
expressive than many of the formats it converts between, one should not
expect perfect conversions between every format and every other. Pandoc
attempts to preserve the structural elements of a document, but not
formatting details such as margin size. And some document elements, such
as complex tables, may not fit into pandoc's simple document model.
While conversions from pandoc's Markdown to all formats aspire to be
perfect, conversions from formats more expressive than pandoc's Markdown
can be expected to be lossy.

Using `pandoc`
--------------
:::

  [Haskell]: https://www.haskell.org
  [Markdown]: http://daringfireball.net/projects/markdown/
  [CommonMark]: http://commonmark.org
  [PHP Markdown Extra]: https://michelf.ca/projects/php-markdown/extra/
  [GitHub-Flavored Markdown]: https://help.github.com/articles/github-flavored-markdown/
  [MultiMarkdown]: http://fletcherpenney.net/multimarkdown/
  [Textile]: http://redcloth.org/textile
  [reStructuredText]: http://docutils.sourceforge.net/docs/ref/rst/introduction.html
  [HTML]: http://www.w3.org/html/
  [LaTeX]: http://latex-project.org
  [MediaWiki markup]: https://www.mediawiki.org/wiki/Help:Formatting
  [TWiki markup]: http://twiki.org/cgi-bin/view/TWiki/TextFormattingRules
  [TikiWiki markup]: https://doc.tiki.org/Wiki-Syntax-Text#The_Markup_Language_Wiki-Syntax
  [Creole 1.0]: http://www.wikicreole.org/wiki/Creole1.0
  [Haddock markup]: https://www.haskell.org/haddock/doc/html/ch03s08.html
  [OPML]: http://dev.opml.org/spec2.html
  [Emacs Org mode]: http://orgmode.org
  [DocBook]: http://docbook.org
  [JATS]: https://jats.nlm.nih.gov
  [Muse]: https://amusewiki.org/library/manual
  [txt2tags]: http://txt2tags.org
  [Vimwiki]: https://vimwiki.github.io
  [EPUB]: http://idpf.org/epub
  [ODT]: http://en.wikipedia.org/wiki/OpenDocument
  [Word docx]: https://en.wikipedia.org/wiki/Office_Open_XML
  [XHTML]: http://www.w3.org/TR/xhtml1/
  [HTML5]: http://www.w3.org/TR/html5/
  [`beamer`]: https://ctan.org/pkg/beamer
  [ConTeXt]: http://www.contextgarden.net/
  [RTF]: http://en.wikipedia.org/wiki/Rich_Text_Format
  [OpenDocument]: http://opendocument.xml.org
  [GNU Texinfo]: http://www.gnu.org/software/texinfo/
  [DokuWiki markup]: https://www.dokuwiki.org/dokuwiki
  [ZimWiki markup]: http://zim-wiki.org/manual/Help/Wiki_Syntax.html
  [FictionBook2]: http://www.fictionbook.org/index.php/Eng:XML_Schema_Fictionbook_2.1
  [groff man]: http://man7.org/linux/man-pages/man7/groff_man.7.html
  [groff ms]: http://man7.org/linux/man-pages/man7/groff_ms.7.html
  [AsciiDoc]: http://www.methods.co.nz/asciidoc/
  [InDesign ICML]: https://www.adobe.com/content/dam/Adobe/en/devnet/indesign/cs55-docs/IDML/idml-specification.pdf
  [TEI Simple]: https://github.com/TEIC/TEI-Simple
  [PowerPoint]: https://en.wikipedia.org/wiki/Microsoft_PowerPoint
  [Slidy]: http://www.w3.org/Talks/Tools/Slidy/
  [Slideous]: http://goessner.net/articles/slideous/
  [DZSlides]: http://paulrouget.com/dzslides/
  [reveal.js]: http://lab.hakim.se/reveal-js/
  [S5]: http://meyerweb.com/eric/tools/s5/
  [PDF]: https://www.adobe.com/pdf/
  [pandoc filters]: http://pandoc.org/filters.html

Installing
----------

Here's [how to install pandoc].

  [how to install pandoc]: INSTALL.md

Documentation
-------------

Pandoc's website contains a full [User's Guide]. It is also available
[here] as pandoc-flavored Markdown. The website also contains some
[examples of the use of pandoc] and a limited [online demo].

  [User's Guide]: https://pandoc.org/MANUAL.html
  [here]: MANUAL.txt
  [examples of the use of pandoc]: https://pandoc.org/demos.html
  [online demo]: https://pandoc.org/try

Contributing
------------

Pull requests, bug reports, and feature requests are welcome. Please
make sure to read [the contributor guidelines] before opening a new
issue.

  [the contributor guidelines]: CONTRIBUTING.md

License
-------

© 2006-2017 John MacFarlane (jgm@berkeley.edu). Released under the
[GPL], version 2 or greater. This software carries no warranty of any
kind. (See COPYRIGHT for full copyright and warranty notices.)

  [GPL]: http://www.gnu.org/copyleft/gpl.html
    "GNU General Public License"
