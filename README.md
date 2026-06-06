# Visual Studio Code Plus Scheme

[![Package Control](https://img.shields.io/packagecontrol/dt/Visual%20Studio%20Code%20Plus%20Scheme?label=Package%20Control)](https://packagecontrol.io/packages/Visual%20Studio%20Code%20Plus%20Scheme)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE.md)
![Sublime Text](https://img.shields.io/badge/Sublime%20Text-2%2F3%2F4-orange)

A colour scheme for Sublime Text that recreates the syntax highlighting from the default installation of **Visual Studio Code**. It is a faithful port of VS Code's *Dark+* and *Light+* token colours.

The package ships two schemes, which appear in Sublime's colour-scheme picker as:

| Picker name | File |
|-------------|------|
| **Dark+**   | `Dark+.sublime-color-scheme` |
| **Light+**  | `Light+.sublime-color-scheme` |

## Screenshots

| | Dark+ | Light+ |
|---|---|---|
| **PHP** | ![PHP dark](https://raw.githubusercontent.com/vbasky/sublime-vscode-plus/master/previews/php-dark.png) | ![PHP light](https://raw.githubusercontent.com/vbasky/sublime-vscode-plus/master/previews/php-light.png) |
| **HTML** | ![HTML dark](https://raw.githubusercontent.com/vbasky/sublime-vscode-plus/master/previews/html-dark.png) | ![HTML light](https://raw.githubusercontent.com/vbasky/sublime-vscode-plus/master/previews/html-light.png) |
| **JavaScript/Vue** | ![JS dark](https://raw.githubusercontent.com/vbasky/sublime-vscode-plus/master/previews/javascript-dark.png) | ![JS light](https://raw.githubusercontent.com/vbasky/sublime-vscode-plus/master/previews/javascript-light.png) |
| **Python** | ![Python dark](https://raw.githubusercontent.com/vbasky/sublime-vscode-plus/master/previews/python-dark.png) | ![Python light](https://raw.githubusercontent.com/vbasky/sublime-vscode-plus/master/previews/python-light.png) |

## Installation

### Package Control (recommended)

1. Open the Command Palette — <kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> (macOS) or <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> (Windows/Linux).
2. Run **Package Control: Install Package**.
3. Search for **Visual Studio Code Plus Scheme** and press <kbd>Enter</kbd>.

### Manual

1. Download `Dark+.sublime-color-scheme` and `Light+.sublime-color-scheme` from this repository.
2. In Sublime Text, open the Command Palette and run **Preferences: Browse Packages**.
3. Copy both files into the `User` directory.

## Changing the colour scheme

There are two ways to activate or switch between **Dark+** and **Light+**.

### Option 1 — the colour-scheme picker (easiest)

1. Open the Command Palette — <kbd>Cmd</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> (macOS) or <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd> (Windows/Linux).
2. Run **UI: Select Color Scheme**.
3. Start typing `Dark+` or `Light+` and press <kbd>Enter</kbd>. The editor updates live as you arrow through the list, so you can preview before committing.

### Option 2 — edit your settings

Open **Preferences → Settings** and add (or change) the `"color_scheme"` key in the right-hand pane:

```jsonc
{
    // Dark+
    "color_scheme": "Packages/Visual Studio Code Plus Scheme/Dark+.sublime-color-scheme",

    // …or Light+
    // "color_scheme": "Packages/Visual Studio Code Plus Scheme/Light+.sublime-color-scheme",
}
```

> **Note:** If you installed manually, the schemes live under `Packages/User/` instead, so use
> `"Packages/User/Dark+.sublime-color-scheme"`.

### Switching automatically with the OS theme

Sublime Text 4 can follow your operating system's light/dark mode. Use Dark+ at night and Light+ during the day by adding:

```jsonc
{
    "theme": "auto",
    "dark_color_scheme":  "Packages/Visual Studio Code Plus Scheme/Dark+.sublime-color-scheme",
    "light_color_scheme": "Packages/Visual Studio Code Plus Scheme/Light+.sublime-color-scheme",
}
```

### Using it for one language only

To apply the scheme to a single syntax (e.g. just Python), open a file of that type and choose **Preferences → Settings — Syntax Specific**, then add the `"color_scheme"` key there. It will override the global setting for that syntax only.

## Customizing colours

You don't need to edit the package files (those get overwritten on update). Instead, create an overlay:

1. Run **UI: Customize Color Scheme** from the Command Palette.
2. Sublime opens a `<scheme-name>.sublime-color-scheme` file in your `User` folder.
3. Add `variables` or `rules` there — they are merged on top of the base scheme and survive updates.

## Supported languages

Built and tested against the scopes Sublime emits for:

`PHP` · `C` · `C++` · `C#` · `JavaScript`/`Vue` · `Python` · `Java` · `Go` · `Groovy` · `HTML`/`Blade` · `CSS`/`Sass`/`SCSS`/`Less` · `JSON` · `XML` · `Markdown` · `YAML` · `MySQL`

Because the scheme targets standard TextMate scopes (`keyword`, `storage.type`, `entity.name.function`, `entity.name.type`, `string`, `constant.numeric`, …), it works with virtually any language. If a token looks wrong in a specific language, please [open an issue](https://github.com/vbasky/sublime-vscode-plus/issues) with a screenshot and the scope name of the affected token (place the cursor on it and run **Tools → Developer → Show Scope Name**).

## Contributing

Issues and pull requests are welcome. When reporting a colouring problem, include the language, a screenshot, and the scope name of the affected token (**Tools → Developer → Show Scope Name**) so it can be reproduced and fixed quickly.

## About

Created by [Vikram Bhaskaran](https://twitter.com/vikrambhaskar). MIT Licensed — see [LICENSE.md](LICENSE.md).
