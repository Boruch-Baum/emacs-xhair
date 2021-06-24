# xhair.el

 * Highlights the current line and column

 This package simultaneously applies `vline-mode` and `hl-line-mode`,
 with tweaks, to present POINT in highlighted cross-hairs, reporting
 the value of POINT as a message in the echo area. This will remain in
 effect until toggled manually (function `xhair-mode` by default),
 or until the next keypress (function `xhair` by default), or for
 a set interval (function `xhair-flash` by default).

## Dependencies:

   * vline - for `vline-mode`

## Installation:

   1) Evaluate or load or install this file.

   2) Optionally, define a global keybinding or defalias for any of
      the commands you intend to use: `xhair`, `xhair-mode`,
      and/or `xhair-flash`.
```
         (global-set-key (kbd "foo") 'xhair))
         (defalias 'xhair 'foo)
```

## Operation:

   M-x `xhair-mode`  - Apply until manually toggled

   M-x `xhair`       - Apply until next keypress

   M-x `xhair-flash` - Apply for a set interval

   Refer to the function docstrings for further details.

## Configuration:

   M-x `customize-group` <RET> xhair <RET>

   You can customize face `xhair-face`, variable
   `xhair-flash-interval` and variable
   `xhair-eldoc-idle-delay`.

## Compatibility:

  * Tested on Debian Emacs 27 nox.

  * Operates nicely with `yascroll-bar-mode`. It temporarily suspends
    that mode locally in order not to make the buffer display jump
    around.

  * Operates nicely with `eldoc-mode`. It delays eldoc messages to
    give the user time to read the value of POINT from the echo area.

## Feedback:

  * It's best to contact me by opening an 'issue' on the package's
    github repository or, distant second-best, by direct e-mail.

  * Code contributions are welcome and github starring is appreciated.

## Antecedent:

   This package is based upon `crosshairs.el' by Drew Adams, available at:

     https://www.emacswiki.org/emacs/download/crosshairs.el

  Its main differences from Drew's package is that it:
  * Is MELPA-friendly
  * Reduces dependencies
  * Reduces features (notably: `crosshairs-toggle-when-idle`)
  * Simplifies code-base
  * Applies a single unique face, by default
  * Suspends `yascroll-bar-mode`, to not interfere with `vline-mode`
  * Reports POINT for all navgitaion for duration of mode
  * Delays `eldoc-mode` messages, to not interfere with reporting POINT
  * Suppresses output to *Messages* buffer
  * Changes documentation
  * Eschews all use of macro `define-minor-mode'

## Colophon:

* Copyright (C) 2021 Boruch Baum <boruch-baum@gmx.com>
* Author/Maintainer:  Boruch Baum <boruch-baum@gmx.com>
* Homepage: https://github.com/Boruch-Baum/emacs-xhair
* License: GPL3+

## Some other Emacs software that I've published

* Diredc [![MELPA](https://melpa.org/packages/diredc-badge.svg)](https://melpa.org/#/diredc) [![MELPA Stable](https://stable.melpa.org/packages/diredc-badge.svg)](https://stable.melpa.org/#/diredc)
  * Large collection of interoperable dired extensions
  * https://github.com/Boruch-Baum/emacs-diredc

* Crossword
  [![MELPA](https://melpa.org/packages/crossword-badge.svg)](https://melpa.org/#/crossword)
  [![MELPA Stable](https://stable.melpa.org/packages/crossword-badge.svg)](https://stable.melpa.org/#/crossword)
  * Download and play crossword puzzles, in Emacs!
  * https://github.com/Boruch-Baum/emacs-crossword

* Emacs-w3m
  * Extensions to the classic web browser (fork)
    * Advanced downloader (bulk, regex, queue management, resume aborted)
    * Scrub history
    * More ...
  * https://github.com/Boruch-Baum/emacs-w3m

* Key-assist
  [![MELPA](https://melpa.org/packages/key-assist-badge.svg)](https://melpa.org/#/key-assist)
  [![MELPA Stable](https://stable.melpa.org/packages/key-assist-badge.svg)](https://stable.melpa.org/#/key-assist)
  * Simple keybinding cheatsheet and launcher
  * https://github.com/Boruch-Baum/emacs-key-assist

* Cursor-flash
  * Highlight the cursor on buffer/window-switch
  * https://github.com/Boruch-Baum/emacs-cursor-flash

* Home-end
  [![MELPA](https://melpa.org/packages/home-end-badge.svg)](https://melpa.org/#/home-end)
  [![MELPA Stable](https://stable.melpa.org/packages/home-end-badge.svg)](https://stable.melpa.org/#/home-end)
  * Turn home and end keys to multi-use navigation keys
  * https://github.com/Boruch-Baum/emacs-home-end

* Keypress-multi-event
  [![MELPA](https://melpa.org/packages/keypress-multi-event-badge.svg)](https://melpa.org/#/keypress-multi-event)
  [![MELPA Stable](https://stable.melpa.org/packages/keypress-multi-event-badge.svg)](https://stable.melpa.org/#/keypress-multi-event)
  * perform different actions when repeating a key
  * https://github.com/Boruch-Baum/emacs-keypress-multi-event

* Post-mode  - Updates to the abandoned email editing package (fork)
  * https://github.com/Boruch-Baum/post-mode
