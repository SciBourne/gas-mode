# GNU Assembler Emacs mode

GAS mode is a major mode for editing assembly code with AT&T syntax, usually code written to be executed by GAS (**G**nu **AS**sembler).

*Forked from: https://codeberg.org/Enocstocks/gas-mode.el*

<br>

## Authors

| Name | User | E-mail |
| --- | --- | --- |
| Bryan Hernández | @Enocstocks | masterenoc@tutamail.com |
| Alexander Marchenko | @SciBourne | bourne-sci-hack@yandex.ru |


<br>
<br>


## Install
First you need to clone this repository and move `gas-menu.el` file to your load path and add the following code to your Emacs config file:

```elisp
(require 'gas-mode)
(add-to-list 'auto-mode-alist '("\\.asm\\'" . gas-mode))
```

Now each time you open a file with `.asm` extension, **gas-mode** will be use automatically.


<br>
<br>


## Customization
Variables can be changed through the customization menu or change its value in your Emacs config files.

<br>

`gas-initial-indentation`

This is an integer used to indent `.section` sections and tags to the `0` column by default but it can be changed to any other column you want.

<br>

`gas-indentation`

This is an integer use to indent any other lines not mentioned by the previous variable, e.g. the instructions or directive lines.


<br>
<br>


## List of TODO improvements or features

* Keep improving indentation, tags can be tricky to indent since its use can be in single line (as memory address identifier for a value) or multi-line (as a memory address where a set of instructions begin or like the single line use)
* Add blinking and indentation to some nested directives like .macro. This idea is dropped since I noticed that I have to use either smie for this mode or make a custom function that evaluates all (or limited amount) the text before point after each keystroke searching for its respective close parenthesis (smie does this)
* Add support for company
* Add support for imenu
