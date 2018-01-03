# eldoc-overlay

Eldoc displays the function signature of the closest function call
around point either in the minibuffer or in the modeline.  This
package modifies Eldoc to display this documentation inline using a
buffer text overlay.

`eldoc-overlay-mode` is a per-buffer minor mode.  
   A call to `eldoc-overlay-enable` turns it on.  
   A call to `eldoc-overlay-disable` turns it off

   <kbd>C-x C-h</kbd> interactively calls `eldoc-overlay-toggle` and tells
   you the mode's new state.

`global-eldoc-overlay-mode` can be used to toggle this for all buffers.  
   A call to `global-eldoc-overlay-enable` turns it on.  
   A call to `global-eldoc-overlay-disable` turns it off

   <kbd>C-u C-x C-h</kbd> interactively calls `global-eldoc-overlay-toggle` and tells
   you the mode's new state.

By default, the overlay is not used in the minibuffer, eldoc is shown in the modeline
in this case.  Set the option `eldoc-overlay-in-minibuffer-flag` non-nil if you want
to enable overlay use in the minibuffer.

The key used to toggle the mode can be customized by setting the `eldoc-overlay-key`
option.

# Installation

```emacs-lisp
(use-package eldoc-overlay
  :ensure t
  :config
  (global-eldoc-overlay-mode 1))
```

# Usage

Eldoc displays the function signature of the closest function call around point
either in the minibuffer or in the modeline.

This package modifies Eldoc to display this documentation inline using a buffer
text overlay.

- `eldoc-overlay-mode` is a per-buffer minor mode.
- A call to `eldoc-overlay-enable' turns it on.
- A call to `eldoc-overlay-disable' turns it off

{C-x C-h} interactively calls `eldoc-overlay-toggle' and tells you the mode's
new state.

- `global-eldoc-overlay-mode' can be used to toggle this for all buffers.
- A call to `global-eldoc-overlay-enable' turns it on.
- A call to `global-eldoc-overlay-disable' turns it off

{C-u C-x C-h} interactively calls `global-eldoc-overlay-toggle` and tells you
the mode's new state.

By default, the overlay is not used in the minibuffer, eldoc is shown in the
modeline in this case. Set the option `eldoc-overlay-in-minibuffer-flag` non-nil
if you want to enable overlay use in the minibuffer.

The key used to toggle the mode can be customized by setting the
`eldoc-overlay-key` option.

Finally, see the documentation for `eldoc-overlay-backend` if you want to try a
different overlay display package backend.

# Changelog

## break backward compatible upgrading changes


This source code originally came from an answer to [justbur](https://emacs.stackexchange.com/users/14114/justbur)
of this [question](https://emacs.stackexchange.com/questions/29256/display-eldoc-help-info-behind-point).

# Screenshots

![eldoc-overlay screenshot](eldoc-overlay.png)
