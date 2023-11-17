[![Melpa Status](http://melpa.org/packages/ruff-format-badge.svg)](http://melpa.org/#/ruff-format)

# ruff-format.el

This Emacs library provides commands and a minor mode for easily
reformatting Python source code using [Ruff][ruff].

# Installation

If you choose not to use one of the convenient packages in
[MELPA][melpa], you'll need to add the directory containing `ruff-format.el`
to your `load-path`, and then `(require 'ruff-format)`.

[`reformatter`][reformatter] is required.

# Usage

Customise the `ruff-format-command` variable as desired, then call
`ruff-format-buffer` or `ruff-format-region` as convenient.

Enable `ruff-format-on-save-mode` in Python mode buffers like this:

```el
(add-hook 'python-mode-hook 'ruff-format-on-save-mode)
```

...or locally to your project with a form in your `.dir-locals.el`
like this:

```el
((python-mode
   (mode . ruff-format-on-save)))
```

# License

SPDX-License-Identifier: GPL-3.0-or-later

[melpa]: http://melpa.org
[reformatter]: https://github.com/purcell/emacs-reformatter
[ruff]: https://docs.astral.sh/ruff/
