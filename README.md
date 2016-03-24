# turkish-mode for Emacs

This Emacs mode is developed by [Deniz Yüret](http://denizyuret.blogspot.com/2006/11/emacs-turkish-mode.html).

This is for people trying to type Turkish documents on a U.S. keyboard
using Emacs. The program provides a turkish-mode in which the correct
Turkish accents are added to the ascii version of the last word typed
each time the user hits space. The latest version is available here.

It was inspired by Gökhan Tür's deasciifier.

The program uses decision lists (included at the end of this file)
which was created based on 1 million words of Turkish news text using
the GPA algorithm. For more information on GPA see the [Greedy prepend
algorithm for decision list induction](http://denizyuret.blogspot.com/2006/11/greedy-prepend-algorithm-for-decision.html).


## Installation

To activate the program first load this file into emacs:

If you have `melpa` and `emacs24` installed, simply type:

	M-x package-install turkish

Add following lines to your init file:

    (require 'turkish)

Then turn on the turkish mode:

    M-x turkish-mode

When Turkish mode is enabled, the space, tab, and enter keys correct
the previous word by adding Turkish accents. For corrections use C-t
to toggle the accent of the character under the cursor.

## About Unicode and UTF-8

Please read the remarks of Deniz Yüret about the Unicode and utf-8
issue and changes between Emacs 23 and previous versions (the following comment
is about turkish-char-alist data structure):

    ;; deniz 20100217: Emacs 23 seems to have changed its internal
    ;; representation to unicode.  So I am adding unicode as another
    ;; column after utf-8.  The columns now are: ascii, latin-5, multibyte
    ;; latin-5, utf-8, unicode.  Emacs versions older than 23 should use
    ;; column 3 (utf8), 23 and later should use column 4 (unicode).


