00readme.txt for amsrefs 2.0 [2004-06-30]

See also install.txt and manifest.txt. There is a history of changes at
the end of this file.

Please send bug reports and questions to tech-support@ams.org.

========================================================================

The amsrefs package deals with bibliographies and citations in LaTeX
documents. The basic citation command remains more or less the same as
in standard LaTeX (\cite), but a number of additional variations address
certain known pitfalls or gaps in the standard LaTeX set of citation
features.

The command for bibliography items is different---\bib instead of
\bibitem---for reasons that will be evident upon further reading in the
documentation.

A set of BibTeX style files are provided to allow people to extract
data from .bib files and produce .bbl files in amsrefs format instead
of conventional \bibitem format.

User documentation is in amsrdoc.pdf.

Technical documentation (including documentation for package writers)
is in amsrefs.pdf.

========================================================================
I. FEATURES

---Preservation of structure.

The internal structural information of the bibliography entries is not
lost when they are imported from the database file into the LaTeX
document. This takes on its greatest significance when archiving
documents in LaTeX form or transmitting them to another user (such as a
publisher).

---Deferred formatting.

This means that the style of the bibliography can be changed on demand
without reimporting everything from the original database(s).

---More natural data format for titles.

Proper nouns do not need to have braces added to prevent capitalization
problems.

---Less ambiguous format for author names.

When author names are given in inverted order (last name first) it is
possible for LaTeX to unambiguously identify the last name without any
further markup, even in cases like Saunders Mac Lane (Mac Lane,
Saunders) versus Stephen H. Lane (Lane, Stephen H.), or Cam Van Tran
(Tran, Cam Van) versus Bert Van Keulen (Van Keulen, Bert). In
BibTeX some of these would need to have extra braces added to ensure
that the surname is accurately distinguished.

---Author-year citations.

There is integrated support for citations in author-year form.

---Back-reference support.

Works in conjunction with the hyperref package.

---Setup requires only LaTeX knowledge.

All bibliography setup can be done in LaTeX; learning another
programming language (such as, the one used in BibTeX bst files) is
unnecessary.

---Self-printable database files.

A LaTeX document that contains only a bibliography in amsrefs forms can
be used as a database for exporting entries to other documents. And
because it is a LaTeX document, the database can be printed directly at
any time simply by running it through LaTeX in the usual way.

---Self-contained.

In many cases it seems possible to do without BibTeX entirely. For
example, if the entries are extracted from a single database file that
is maintained in sorted order, the bibliography can be printed directly
by LaTeX on the first pass and the citations resolved on the second
pass.

========================================================================
II. GETTING STARTED

1. Install the package, referring to install.txt as needed.

2. There are four example files provided:

  cite-xa : Demonstrates an author-year citation scheme. The
            bibliography is embedded in the .tex file instead of
            residing in a separate .bbl file.

  cite-xb : Demonstrates usage with more-or-less standard BibTeX
            methods.

  cite-xs : Shows how the bbl file can be created by LaTeX itself from a
            suitably presorted ltb file.

  cite-xh : A working hyperref/backrefs example.

3. Run LaTeX on cite-xa.tex. Take a look at the messages that have to do
with citations and the bibliography section. Run LaTeX again to resolve
the citations and check the output.

4. Run LaTeX on cite-xb.tex. Run BibTeX. Look at the bbl file.
Interesting, huh? Run LaTeX twice more to resolve the citations.

5. Run LaTeX on cite-xs.tex and look at the output.

6. Run pdflatex on cite-xh.tex (it is set up to use BibTeX also, like
cite-xb).

========================================================================
III. REMARKS ON THIS RELEASE

This is a thorough overhaul and rewrite of the the amsrefs package.
Many (perhaps even most) of the internals have changed and a number of
new features have been added.  Backwards compatibility for documents
created with previous versions of this package has been

See changes.pdf for information on the user-visible changes.

========================================================================
IV. SETTING UP A CUSTOM BIBLIOGRAPHY STYLE

More documentation is needed here, but the discussion in amsrefs.pdf
should be enough to get you started.  See especially sections 4, 6.10,
6.26.15, and 6.27.

========================================================================
V. CHANGE LOG

*amsrefs.dtx 2.0 2004-06-30 11:24:39 EDT

Major rewrite of internals.  See changes.pdf for information on the
user-visible changes.
