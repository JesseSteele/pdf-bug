# pdf-bug
## Example of the problem converting a document with Greek into pdf

This problem originated with a .doc file for publishing on Smashwords and Amazon's KDP. But, the problem is identical with .odt files in LibreOffice Writer.

The problem: Using standard Roman fonts, everything is fine. Using TexGyre's Pagells font in LibreOffice (and other Linux odt > pdf command line converters), Greek words get unexpected spaces in the words, thus these words can get pushed OUTSIDE the margins! They should at least wrap. This creates a double problem for publishers: a space wrongly appearing in a single word & printing ourside the margine.

*TexGyre Pagella & TexGyre Schola are from the Gust Foundary, an awesome free fonts, book printing quality, highly recommended.*

*It is important for publishers to be able to use good book fonts, such as TexGyre Pagella, for real publishing, not only [hard to read] standard Roman fonts.*

The only way I made the book with Greek work correctly was to use .odt in Calligra Words, correct Calligra's querks, then export it to Custom-sized .pdf. But, Calligra has page number problems when exporting to .pdf from .doc. LibreOffice is equally problematic. I have at least ten other books printable via Amazon, all done with LibreOffice, and they have no problems with TexGyre Pagella because those books don't have Greek words.

If Calligra can do it from .odt, then it's not a font problem. This is a pdf engine problem.

### Files & Descriptions

`Problem example.odt` & `Problem example.doc` are the source files for the conversions. They contain book-style page numbers (i, ii for Introduction, then 1, 2, from Chapter One) as well as the Pagella and standard Roman fonts.

`Problem example ODT - via LibreOffice.pdf` & `Problem example DOC - via LibreOffice.pdf` were made via LibreOffice Writer, from .odt and .doc respectively. The Pagella font problem shows in the spaces in the Greek words, but not in the standard Roman font.

`Problem example ODT - via Calligra.pdf` & `Problem example DOC - via Calligra.pdf` were made via Calligra Words, from .odt and .doc respectively. The Pagella font has no problems, but using the .doc file as a source messes up the page numbers.

These other command line tooles were used, all of them had similar failures:

`unoconv` `abiword` `lowriter`

`pandoc` (required `pdflatex`, dunno where to get)
