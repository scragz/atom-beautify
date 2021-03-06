# :lipstick: [atom-beautify](https://github.com/Glavin001/atom-beautify)
[![GitHub issues](https://img.shields.io/github/issues/Glavin001/atom-beautify.svg?style=flat-square)](https://github.com/Glavin001/atom-beautify/issues)
[![GitHub stars](https://img.shields.io/github/stars/Glavin001/atom-beautify.svg?style=flat-square)](https://github.com/Glavin001/atom-beautify/stargazers)
[![Gitter](https://img.shields.io/gitter/room/Glavin001/atom-beautify.svg?style=flat-square)](https://gitter.im/Glavin001/atom-beautify)
[![Bountysource](https://img.shields.io/bountysource/team/atom-beautify/activity.svg?style=flat-square)](https://www.bountysource.com/teams/atom-beautify)
[![Paypal Donations](https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=X2RK5DKN6YXPJ&lc=CA&item_name=Atom%2dBeautify&item_number=atom%2dbeautify&currency_code=CAD&bn=PP%2dDonationsBF%3abtn_donate_LG%2egif%3aNonHosted)

| Mac OS <img src="https://cloud.githubusercontent.com/assets/1885333/17059766/2530c9d8-4ffd-11e6-9529-3fa47dbff616.png" width="50px"> and <img src="https://cloud.githubusercontent.com/assets/1885333/17059750/11c4474e-4ffd-11e6-89e1-2486ca5b3234.png" width="100px"> | <img src="https://cloud.githubusercontent.com/assets/1885333/17059763/206a7d4a-4ffd-11e6-859e-7856902fb300.png" width="100px"> |
| --- | --- |
| [Travis CI: ![Travis branch](https://img.shields.io/travis/Glavin001/atom-beautify/master.svg?style=flat-square)](https://travis-ci.org/Glavin001/atom-beautify) | [AppVeyor: ![AppVeyor branch](https://img.shields.io/appveyor/ci/Glavin001/atom-beautify/master.svg?style=flat-square)](https://ci.appveyor.com/project/Glavin001/atom-beautify) |

[![Throughput Graph](https://graphs.waffle.io/Glavin001/atom-beautify/throughput.svg)](https://waffle.io/Glavin001/atom-beautify/metrics)

> Beautify HTML, CSS, JavaScript, PHP, Python, Ruby, Java, C, C++, C#, Objective-C, CoffeeScript, TypeScript, Coldfusion, SQL, and more in Atom

| Before | After |
| --- | ---- |
| Original HTML | Beautified HTML |
| ![image](https://cloud.githubusercontent.com/assets/1885333/16542727/db52adc6-408a-11e6-824e-04aed06bd2f7.png) | ![image](https://cloud.githubusercontent.com/assets/1885333/16542728/dcac3700-408a-11e6-8e35-9c8fc4432edc.png) |

## Table of Contents

- [Installation](#installation)
- [Beautifiers](#beautifiers)
- [Language Support](#language-support)
- [Usage](#usage)
  - [Command Palette](#command-palette)
    - [Beautify a Specific Language](#beautify-a-specific-language)
  - [Selection of Code](#selection-of-code)
  - [Beautify On Save](#beautify-on-save)
  - [Keyboard Shortcut](#keyboard-shortcut)
    - [Custom Keyboard Shortcuts](#custom-keyboard-shortcuts)
- [Configuration](#configuration)
  - [Simple](#simple)
  - [Nested](#nested-recommended)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)

## Installation

Atom Package: https://atom.io/packages/atom-beautify

```bash
apm install atom-beautify
```

Or Settings/Preferences ➔ Packages ➔ Search for `atom-beautify`

### Important Notice: Analytics

[Atom-Beautify respects the `core.telemetryConsent` configuration option from Atom editor.](https://github.com/Glavin001/atom-beautify/issues/1179)
If you do not wish to have usage data sent to Google Analytics then please set `core.telemetryConsent` to `no` or `undecided` option before using Atom-Beautify.
See [`Anonymous Analytics` section of docs](docs/options.md#anonymous-analytics) for details.
Thank you.

| On Atom Load | Change Setting Later |
| --- | --- |
| ![image](https://cloud.githubusercontent.com/assets/1885333/25234140/947b1b50-25b7-11e7-8ebc-0ae37420f13e.png) | ![image](https://cloud.githubusercontent.com/assets/1885333/25234184/b41b4192-25b7-11e7-8185-a83829b48078.png) |


### Next Version: [Unibeautify](https://github.com/Unibeautify/unibeautify)

Atom-Beautify is going to be completely rewritten with [Unibeautify](https://github.com/Unibeautify/unibeautify) at its core!
See [`unibeautify` branch](../../tree/unibeautify) for work in progress and [Issue #1174](https://github.com/Glavin001/atom-beautify/issues/1174).

## Beautifiers

Some of the supported beautifiers are developed for Node.js and are automatically installed when Atom-Beautify is installed. However, other beautifiers are command-line interface (CLI) applications and require you to manually install them.

| Beautifier | Is Pre-Installed? | Installation Instructions |
| --- | --- | --- |
| align-yaml | :white_check_mark: | Nothing! |
| autopep8 | :x: | Go to https://github.com/hhatto/autopep8 and follow the instructions. |
| beautysh | :x: | Go to https://github.com/bemeurer/beautysh and follow the instructions. |
| clang-format | :x: | Go to https://clang.llvm.org/docs/ClangFormat.html and follow the instructions. |
| cljfmt | :white_check_mark: | Nothing! |
| Coffee Formatter | :white_check_mark: | Nothing! |
| coffee-fmt | :white_check_mark: | Nothing! |
| Crystal | :x: | Go to http://crystal-lang.org and follow the instructions. |
| CSScomb | :white_check_mark: | Nothing! |
| dfmt | :x: | Go to https://github.com/Hackerpilot/dfmt and follow the instructions. |
| elm-format | :x: | Go to https://github.com/avh4/elm-format and follow the instructions. |
| erl_tidy | :x: | Go to http://erlang.org/doc/man/erl_tidy.html and follow the instructions. |
| ESLint Fixer | :white_check_mark: | Nothing! |
| formatR | :x: | Go to https://github.com/yihui/formatR and follow the instructions. |
| Fortran Beautifier | :x: | Go to https://www.gnu.org/software/emacs/ and follow the instructions. |
| Gherkin formatter | :white_check_mark: | Nothing! |
| gofmt | :x: | Go to https://golang.org/cmd/gofmt/ and follow the instructions. |
| hh_format | :x: | Go to http://hhvm.com/ and follow the instructions. |
| HTML Beautifier | :x: | Go to https://github.com/threedaymonk/htmlbeautifier and follow the instructions. |
| JS Beautify | :white_check_mark: | Nothing! |
| JSCS Fixer | :white_check_mark: | Nothing! |
| Latex Beautify | :x: | Go to https://github.com/cmhughes/latexindent.pl and follow the instructions. |
| Lua beautifier | :x: | Go to https://www.perl.org/ and follow the instructions. |
| Marko Beautifier | :white_check_mark: | Nothing! |
| Nginx Beautify | :white_check_mark: | Nothing! |
| ocp-indent | :x: | Go to https://www.typerex.org/ocp-indent.html and follow the instructions. |
| Perltidy | :x: | Go to http://perltidy.sourceforge.net/ and follow the instructions. |
| PHP-CS-Fixer | :x: | Go to https://github.com/FriendsOfPHP/PHP-CS-Fixer and follow the instructions. |
| PHPCBF | :x: | Go to http://php.net/manual/en/install.php and follow the instructions. |
| Pretty Diff | :white_check_mark: | Nothing! |
| Pug Beautify | :white_check_mark: | Nothing! |
| puppet-lint | :x: | Go to http://puppet-lint.com/ and follow the instructions. |
| pybeautifier | :x: | Go to https://github.com/guyskk/pybeautifier and follow the instructions. |
| Remark | :white_check_mark: | Nothing! |
| Rubocop | :x: | Go to https://github.com/bbatsov/rubocop and follow the instructions. |
| Ruby Beautify | :x: | Go to https://github.com/erniebrodeur/ruby-beautify and follow the instructions. |
| rustfmt | :x: | Go to https://github.com/nrc/rustfmt and follow the instructions. |
| SassConvert | :x: | Go to http://sass-lang.com/documentation/file.SASS_REFERENCE.html#syntax and follow the instructions. |
| sqlformat | :x: | Go to https://github.com/andialbrecht/sqlparse and follow the instructions. |
| stylish-haskell | :x: | Go to https://github.com/jaspervdj/stylish-haskell and follow the instructions. |
| Tidy Markdown | :white_check_mark: | Nothing! |
| TypeScript Formatter | :white_check_mark: | Nothing! |
| Uncrustify | :x: | Go to https://github.com/uncrustify/uncrustify and follow the instructions. |
| Vue Beautifier | :white_check_mark: | Nothing! |
| yapf | :x: | Go to https://github.com/google/yapf and follow the instructions. |

## Language Support

See [all supported options in the documentation at  `docs/options.md`](docs/options.md).

| Language | Grammars | File Extensions | Supported Beautifiers |
| --- | --- | --- | ---- |
| Apex | `Apex` |`.cls`, `.trigger` | [`Uncrustify`](https://github.com/uncrustify/uncrustify) (Default) |
| Arduino | `Arduino` |`.ino`, `.pde` | [`Uncrustify`](https://github.com/uncrustify/uncrustify) (Default) |
| Bash | `Shell Script` |`.bash`, `.sh` | [`beautysh`](https://github.com/bemeurer/beautysh) (Default) |
| C | `C`, `opencl` |`.h`, `.c`, `.cl` | [`Uncrustify`](https://github.com/uncrustify/uncrustify) (Default), [`clang-format`](https://clang.llvm.org/docs/ClangFormat.html) |
| Coldfusion | `html` |`.cfm`, `.cfml`, `.cfc` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| Clojure | `Clojure` |`.clj`, `.cljs`, `.edn` | [`cljfmt`](https://github.com/snoe/node-cljfmt) (Default) |
| CoffeeScript | `CoffeeScript` |`.coffee` | [`Coffee Formatter`](https://github.com/Glavin001/Coffee-Formatter), [`coffee-fmt`](https://github.com/sterpe/coffee-fmt) (Default) |
| C++ | `C++` |`.h`, `.hh`, `.cc`, `.cpp`, `.cxx`, `.C`, `.cu`, `.c++`, `.hpp`, `.hxx`, `.h++`, `.cuh` | [`Uncrustify`](https://github.com/uncrustify/uncrustify) (Default), [`clang-format`](https://clang.llvm.org/docs/ClangFormat.html) |
| Crystal | `Crystal` |`.cr` | [`Crystal`](http://crystal-lang.org) (Default) |
| C# | `C#` |`.cs` | [`Uncrustify`](https://github.com/uncrustify/uncrustify) (Default) |
| CSS | `CSS` |`.css` | [`CSScomb`](https://github.com/csscomb/csscomb.js), [`JS Beautify`](https://github.com/beautify-web/js-beautify) (Default), [`Pretty Diff`](https://github.com/prettydiff/prettydiff), [`SassConvert`](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#syntax) |
| CSV | `CSV` |`.csv` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| D | `D` |`.d` | [`Uncrustify`](https://github.com/uncrustify/uncrustify) (Default), [`dfmt`](https://github.com/Hackerpilot/dfmt) |
| EJS | `EJS`, `JavaScript Template`, `HTML (Angular)` |`.ejs` | [`JS Beautify`](https://github.com/beautify-web/js-beautify) (Default), [`Pretty Diff`](https://github.com/prettydiff/prettydiff) |
| Elm | `Elm` |`.elm` | [`elm-format`](https://github.com/avh4/elm-format) (Default) |
| ERB | `HTML (Ruby - ERB)`, `HTML (Rails)` |`.erb` | [`HTML Beautifier`](https://github.com/threedaymonk/htmlbeautifier), [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| Erlang | `Erlang` |`.erl` | [`erl_tidy`](http://erlang.org/doc/man/erl_tidy.html) (Default) |
| Fortran | `Fortran - Modern` |`.f90`, `.F90`, `.f95`, `.F95` | [`Fortran Beautifier`](https://www.gnu.org/software/emacs/) (Default) |
| gherkin | `Gherkin` |`.feature` | [`Gherkin formatter`](https://github.com/Glavin001/atom-beautify/blob/master/src/beautifiers/gherkin.coffee) (Default) |
| GLSL | `C`, `opencl`, `GLSL` |`.vert`, `.frag` | [`clang-format`](https://clang.llvm.org/docs/ClangFormat.html) (Default) |
| Go | `Go` |`.go` | [`gofmt`](https://golang.org/cmd/gofmt/) (Default) |
| Golang Template | `HTML (Go)`, `Go Template` |`.gohtml` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| Handlebars | `Handlebars`, `HTML (Handlebars)` |`.hbs`, `.handlebars` | [`JS Beautify`](https://github.com/beautify-web/js-beautify) (Default), [`Pretty Diff`](https://github.com/prettydiff/prettydiff) |
| Haskell | `Haskell` |`.hs` | [`stylish-haskell`](https://github.com/jaspervdj/stylish-haskell) (Default) |
| HTML | `HTML` |`.html` | [`JS Beautify`](https://github.com/beautify-web/js-beautify) (Default), [`Pretty Diff`](https://github.com/prettydiff/prettydiff) |
| Jade | `Jade`, `Pug` |`.jade`, `.pug` | [`Pug Beautify`](https://github.com/vingorius/pug-beautify) (Default) |
| Java | `Java` |`.java` | [`Uncrustify`](https://github.com/uncrustify/uncrustify) (Default) |
| JavaScript | `JavaScript` |`.js` | [`ESLint Fixer`](https://github.com/eslint/eslint), [`JS Beautify`](https://github.com/beautify-web/js-beautify) (Default), [`JSCS Fixer`](https://github.com/jscs-dev/node-jscs/), [`Pretty Diff`](https://github.com/prettydiff/prettydiff) |
| JSON | `JSON` |`.json` | [`JS Beautify`](https://github.com/beautify-web/js-beautify) (Default), [`Pretty Diff`](https://github.com/prettydiff/prettydiff) |
| JSX | `JSX`, `JavaScript (JSX)`, `Babel ES6 JavaScript`, `JavaScript with JSX` |`.jsx`, `.js` | [`JS Beautify`](https://github.com/beautify-web/js-beautify), [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| LaTeX | `BibTeX`, `LaTeX`, `TeX` |`.bib`, `.tex`, `.sty`, `.cls`, `.dtx`, `.ins`, `.bbx`, `.cbx` | [`Latex Beautify`](https://github.com/cmhughes/latexindent.pl) (Default) |
| LESS | `LESS` |`.less` | [`CSScomb`](https://github.com/csscomb/csscomb.js), [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| Lua | `Lua` |`.lua` | [`Lua beautifier`](https://www.perl.org/) (Default) |
| Markdown | `GitHub Markdown` |`.markdown`, `.md` | [`Remark`](https://github.com/wooorm/remark), [`Tidy Markdown`](https://github.com/slang800/tidy-markdown) (Default) |
| Marko | `Marko` |`.marko` | [`Marko Beautifier`](https://github.com/marko-js/marko-prettyprint) (Default) |
| Mustache | `HTML (Mustache)` |`.mustache` | [`JS Beautify`](https://github.com/beautify-web/js-beautify) (Default), [`Pretty Diff`](https://github.com/prettydiff/prettydiff) |
| Nginx | `nginx` |`.conf` | [`Nginx Beautify`](https://github.com/denysvitali/nginxbeautify) (Default) |
| Nunjucks | `Nunjucks`, `Nunjucks Templates`, `HTML (Nunjucks Templates)` |`.njk`, `.nunjucks` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| Objective-C | `Objective-C`, `Objective-C++` |`.m`, `.mm`, `.h` | [`Uncrustify`](https://github.com/uncrustify/uncrustify) (Default), [`clang-format`](https://clang.llvm.org/docs/ClangFormat.html) |
| OCaml | `OCaml` |`.ml` | [`ocp-indent`](https://www.typerex.org/ocp-indent.html) (Default) |
| Pawn | `Pawn` | | [`Uncrustify`](https://github.com/uncrustify/uncrustify) (Default) |
| Perl | `Perl`, `Perl 6` |`.pl`, `.PL`, `.pm`, `.pod`, `.t` | [`Perltidy`](http://perltidy.sourceforge.net/) (Default) |
| PHP | `PHP` |`.php`, `.module`, `.inc` | [`PHP-CS-Fixer`](https://github.com/FriendsOfPHP/PHP-CS-Fixer) (Default), [`PHPCBF`](http://php.net/manual/en/install.php), [`hh_format`](http://hhvm.com/) |
| Puppet | `Puppet` |`.pp` | [`puppet-lint`](http://puppet-lint.com/) (Default) |
| Python | `Python` |`.py` | [`autopep8`](https://github.com/hhatto/autopep8) (Default), [`pybeautifier`](https://github.com/guyskk/pybeautifier), [`yapf`](https://github.com/google/yapf) |
| R | `R` |`.r`, `.R` | [`formatR`](https://github.com/yihui/formatR) (Default) |
| Riot.js | `Riot.js`, `HTML (Riot Tag)` |`.tag` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| Ruby | `Ruby`, `Ruby on Rails` |`.rb` | [`Rubocop`](https://github.com/bbatsov/rubocop) (Default), [`Ruby Beautify`](https://github.com/erniebrodeur/ruby-beautify) |
| Rust | `Rust` |`.rs`, `.rlib` | [`rustfmt`](https://github.com/nrc/rustfmt) (Default) |
| Sass | `Sass` |`.sass` | [`SassConvert`](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#syntax) (Default) |
| SCSS | `SCSS` |`.scss` | [`CSScomb`](https://github.com/csscomb/csscomb.js), [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default), [`SassConvert`](http://sass-lang.com/documentation/file.SASS_REFERENCE.html#syntax) |
| Spacebars | `Spacebars` | | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| SQL | `SQL (Rails)`, `SQL` |`.sql` | [`sqlformat`](https://github.com/andialbrecht/sqlparse) (Default) |
| SVG | `SVG` |`.svg` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| Swig | `HTML (Swig)`, `SWIG` |`.swig` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| TSS | `TSS` |`.tss` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| Twig | `HTML (Twig)` |`.twig` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| TypeScript | `TypeScript` |`.ts` | [`TypeScript Formatter`](https://github.com/vvakame/typescript-formatter) (Default) |
| UX Markup | `UX` |`.ux` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| Vala | `Vala` |`.vala`, `.vapi` | [`Uncrustify`](https://github.com/uncrustify/uncrustify) (Default) |
| Visualforce | `Visualforce` |`.page` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| Vue | `Vue Component` |`.vue` | [`Vue Beautifier`](https://github.com/Glavin001/atom-beautify/blob/master/src/beautifiers/vue-beautifier.coffee) (Default) |
| XML | `SLD`, `XML`, `XHTML`, `XSD`, `XSL`, `JSP`, `GSP` |`.sld`, `.xml`, `.xhtml`, `.xsd`, `.xsl`, `.jsp`, `.gsp`, `.plist`, `.recipe`, `.config` | [`JS Beautify`](https://github.com/beautify-web/js-beautify), [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| XTemplate | `XTemplate` |`.xtemplate` | [`Pretty Diff`](https://github.com/prettydiff/prettydiff) (Default) |
| YAML | `YAML` |`.yml`, `.yaml` | [`align-yaml`](https://github.com/jonschlinkert/align-yaml) (Default) |

## Usage

### Command Palette

Open the [Command Palette](https://github.com/atom/command-palette), type `Beautify`, and run `Beautify Editor`.

![image](https://cloud.githubusercontent.com/assets/1885333/16542583/1c8d975c-4085-11e6-8307-e35df7430a10.png)

#### Beautify a Specific Language

You can use the [Command Palette](https://github.com/atom/command-palette) to beautify the editor for a specific language.
The commands are in the form `Atom Beautify: Beautify Language {NAME}` (i.e. `atom-beautify:beautify-language-{NAME}` for keyboard shortcuts).
For example, you may want to beautify `JavaScript` code within a `HTML` file.

![atom-beautify-language-commands](https://cloud.githubusercontent.com/assets/1885333/25775586/f3fc7ec4-327e-11e7-8576-45e735e80032.gif)

### Selection of Code

It will only beautify selected text if a selection is found -- if not, the whole file will be beautified.

| Selection of Code | Beautify Selection of Code | Beautify Entire File |
| --- | --- | --- |
| Select code in Atom editor | Only that selection is beautified | Without a selection all code is beautified |
| ![image](https://cloud.githubusercontent.com/assets/1885333/16542597/b3f90c84-4085-11e6-8a0e-1b8604ae385c.png) | ![image](https://cloud.githubusercontent.com/assets/1885333/16542598/b5a86b10-4085-11e6-80cf-0afaf1a819c3.png) | ![image](https://cloud.githubusercontent.com/assets/1885333/16542603/b798ec24-4085-11e6-880e-8d3a2741940f.png) |

### Beautify On Save

`Beautify On Save` can be enabled for each language individually.

For example, for language `HTML` go into Atom-Beautify's package settings (`Atom` ➔ `Preferences` ➔ Search for `atom-beautify`), find `HTML`, and toggle the `Beautify On Save` option.

![atom-beautify-setup-beautify-on-save](https://cloud.githubusercontent.com/assets/1885333/16542692/3e781e74-4089-11e6-9cf2-5a19af161093.gif)

### Keyboard Shortcut

You can also type <kbd>Ctrl</kbd>-<kbd>Alt</kbd>-<kbd>B</kbd> as a shortcut or click `Packages > Beautify` in the menu.

#### Custom Keyboard Shortcuts

See [Keymaps In-Depth](https://atom.io/docs/latest/behind-atom-keymaps-in-depth) for more details.

For example:

```coffeescript
'.editor':
  'ctrl-alt-b': 'atom-beautify:beautify-editor'
```

## Configuration

Edit your `.jsbeautifyrc` file in any of the following locations:

- Atom Package Settings
  `Atom` ➔ `Preferences` ➔ Search for `atom-beautify`
- Same directory as current file
- Project root
`atom-beautify` will recursively look up from the current file's directory to find `.jsbeautifyrc`.
- Your user's home directory

**Note**: *Comments are supported in `.jsbeautifyrc` thanks to [strip-json-comments](https://github.com/sindresorhus/strip-json-comments).*

See examples of both ways inside [`examples/`](examples)

See [all supported options in the documentation at  `docs/options.md`](docs/options.md).

### Simple

See [examples/simple-jsbeautifyrc/.jsbeautifyrc](examples/simple-jsbeautifyrc/.jsbeautifyrc).

```json
{
  "indent_size": 2,
  "indent_char": " ",
  "other": " ",
  "indent_level": 0,
  "indent_with_tabs": false,
  "preserve_newlines": true,
  "max_preserve_newlines": 2,
  "jslint_happy": true,
  "indent_handlebars": true
}
```

### Nested (Recommended)

See [examples/nested-jsbeautifyrc/.jsbeautifyrc](examples/nested-jsbeautifyrc/.jsbeautifyrc).

```json
{
  "html": {
    "brace_style": "collapse",
    "indent_char": " ",
    "indent_scripts": "normal",
    "indent_size": 6,
    "max_preserve_newlines": 1,
    "preserve_newlines": true,
    "unformatted": ["a", "sub", "sup", "b", "i", "u"],
    "wrap_line_length": 0
  },
  "css": {
    "indent_char": " ",
    "indent_size": 4
  },
  "js": {
    "indent_size": 2,
    "indent_char": " ",
    "indent_level": 0,
    "indent_with_tabs": false,
    "preserve_newlines": true,
    "max_preserve_newlines": 2,
    "jslint_happy": true
  },
  "sql": {
    "indent_size": 4,
    "indent_char": " ",
    "indent_level": 0,
    "indent_with_tabs": false
  }
}
```

## Troubleshooting

See [`docs/troubleshooting.md`](docs/troubleshooting.md).

## Contributing

[See all contributors on GitHub](../../graphs/contributors).

Please update the [CHANGELOG.md](CHANGELOG.md),
add yourself as a contributor to the [package.json](package.json),
and submit a [Pull Request on GitHub](https://help.github.com/articles/using-pull-requests/).

## License

[MIT](LICENSE.md) © [Glavin Wiechert](https://github.com/Glavin001)
