00readme.txt for amsmath 2.0 [2004/08/06] American Mathematical Society

See manifest.txt for a list of all the files in the distribution.

See install.txt for installation instructions. [Installing from an
archive file such as ftp://ftp.ams.org/pub/tex/amsmath.zip is
recommended.]

The amsmath package is an extension package for LaTeX that provides
additional features to facilitate mathematical typesetting. It has been
developed by the American Mathematical Society and released for general
use as a service to the mathematical community. A number of smaller
auxiliary packages are also distributed with the amsmath package.

In order to use amsmath you need to have TeX installed first. TeX is not
an AMS product. For information on getting TeX see one of the following:

  http://www.tug.org/
  http://www.ams.org/tex/tex-resources.html

The primary documentation for amsmath is in

  amsldoc.pdf

Additional documentation files include:

  diffs-m.txt
  subeqn.pdf
  technote.pdf
  testmath.pdf

which are included in the collection.  Additional documentation can be
found in the amsmath FAQ:

  http://www.ams.org/tex/amsmath-faq.html

For technical support:

  American Mathematical Society
  Technical Support
  Publications Technical Group
  P. O. Box 6248
  Providence, RI 02940-6248
  Phone: 800-321-4AMS (321-4267) (USA/Canada) or 401-455-4080
  tech-support@ams.org

For submitting bug reports, however, users are encouraged to use the
standard LaTeX bug reporting system: Issue the command

  latex latexbug.tex

and follow the resulting instructions (selecting the "amslatex" category
when the list of possible categories is shown).

========================================================================
RECENT CHANGES (REVERSE ORDER)

---amsmath.faq - 2004/08/06
Removed from distribution; replaced by on-line FAQ at
http://www.ams.org/tex/amsmath-faq.html

---amsmath.dtx 2.13 2000/07/18:

After the numbering patches in 2.11, \notag failed in certain
circumstances: introduce some more auxiliary functions to sort things
out, and redefine \nonumber.

---amstext.dtx 2.01 2000/06/29:

Use \f@size instead of \tf@size because they are not necessarily the
same and the former is better for putting a few words into a display.

---amsmath.dtx 2.12 2000/06/06:

Fix transposed lines in 2.11 patch.

---amsdtx.dtx - 2000/06/02:

Move to the amscls distribution.

---amsmath.dtx 2.11 2000/06/02:

Prevent "Arithmetic overflow" error by guarding against divide-by-zero
in \x@calc@shift@lc (align environment).

---amsmath.dtx 2.10 2000/05/25:

Clear up error message for \allowdisplaybreaks[0].

Make mathdisplay re-entrant by introducing mathdisplay@stack, to
clear up numbering problems in unusual circumstances such as \[ \]
nested inside minipage inside equation.

---amsmath.dtx 2.09 2000/04/21:

Ensure good catcodes for " etc.

---amsmath.dtx 2.08 2000/03/16:

Fixed erroneous tag placement on split with fleqn/tbtags options.

---amsmath.dtx 2.07 2000/03/15:

Add \reset@strutbox@ to deal with the following bug: After
$...\mbox{\Huge $...$}...$, line spacing is wrong in a following
"gather" or other environment that uses \strut@.

Patch to fix bug with intlimits option: too much space in the middle of
\iint.

Overhaul math accents again to fix a couple of bugs reported by Thimm.

---amsmath.dtx 2.06 2000/03/10:

Change \MathAccent to \mathaccentV so \DeclareMathAccent won't give an
error when redefining an accent.

---amsmath.dtx 2.05 2000/01/06:

Fixed incorrect placement of fleqn/reqno equation numbers inside
indented lists (displaywidth < columnwidth). Changed the
multline/fleqn/leqno indent to match mathmargin when possible instead of
always just using multlinetaggap.
