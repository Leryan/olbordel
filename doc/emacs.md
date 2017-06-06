# Emacs memo

## Docs and blogs

 * https://realpython.com/blog/python/emacs-the-best-python-editor/
 * https://www.philnewton.net/guides/emacs-as-a-php-editor/

## Modes

### MELPA

```
;; INSTALL PACKAGES
;; --------------------------------------

(require 'package)

(add-to-list 'package-archives
       '("melpa" . "http://melpa.org/packages/") t)

(package-initialize)
(when (not package-archive-contents)
  (package-refresh-contents))

(defvar myPackages
  '(pkg1
    pkg2
    pkg3...))

(mapc #'(lambda (package)
    (unless (package-installed-p package)
      (package-install package)))
      myPackages)
```

### elpy, flycheck, py-autopep8

 * `jedi` for completion
 * `autopep8` for pep8
 * `flake8` for flycheck.

### markdown-mode

 * `markdown`

### php

 * `php-cli`
 * `cscope`

## Shortcuts

### General

Shortcut   | Use for
-----------|-----------
`C-x C-f`  | Open new file
`C-x C-c`  | Quit
`C-x C-s`  | Save
`C-spc`    | Select text
`C-w`      | Cut
`M-w`      | Copy
`C-y`      | Paste
`C-/`      | Undo
`C-s`-`C-r`| Search forward-backward

### Move

Shortcut   | Use for
-----------|--------------
`C-n`      | Jump to next line
`C-p`      | Jump to previous line
`C-e`   | Move to EOF
`C-a`   | Move to line start
`M-g g` | Move to line number [input]
`M-g c` | Mot to char number [input]
`M-<`   | Move to buffer start
`M->`   | Move to buffer end

### Buffer

Shortcut      | Use for
--------------|-----------------
`C-x b <name>`| Create/go to buffer
`C-x C-b`     | List buffers
`C-x k <name>`| Kill buffer

### Window

Shortcut| Use for
--------|----------
`C-x 2` | Horizontal window split
`C-x 3` | Vertical window split
`C-x o` | Select another window
`C-x 0` | Kill current window
