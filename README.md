# GNU Assembler Emacs mode

## Overview
Gas mode is a major mode for editing assembly code with AT&T syntax, usually code written to be executed by GAS (Gnu assembler).

<br>

## Install
First you need to clone this repository and move gas-menu.el file to your load path and add the following code to your .emacs file:

```elisp
(require 'gas-mode)
(add-to-list 'auto-mode-alist '("\\.asm\\'" . gas-mode))
```

Now each time you open a file with .asm extension, gas-mode will be use automatically.

<br>

## Customization
Variables can be changed through the customization menu or change its value in your .emacs file.

`gas-initial-indentation`

This is an integer used to indent .section sections and tags to the 0 column by default but it can be changed to any other column you want.


`gas-indentation`

This is an integer use to indent any other lines not mentioned by the previous variable, e.g. the instructions or directive lines.
