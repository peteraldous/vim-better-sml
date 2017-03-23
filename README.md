# vim-better-sml

> Some improvements to the default SML filetype plugins for Vim.


## Install

Install using your favorite plugin manager. For example, to install using
Vundle, add this line to your ~/.vimrc:

```
Plugin 'jez/vim-better-sml'
```

If you're unfamiliar using Vim plugins, check out [Vim as an IDE][vim-ide] which
will get you up to speed.

## Summary

[![Screenshot](sample/example.png)](https://raw.githubusercontent.com/jez/vim-better-sml/master/sample/example.png)

## Features

- Semantic Information
  - Look up type of identifier under cursor (`:SMLTypeQuery`)
  - Jump to definition of identifier under cursor (`:SMLJumpToDef`)
  - Show type errors in sign column
  - Warn about unused variables
- Syntax
  - Various corrections to default syntax highlighting
  - Conceal characters (`'a` to `α`, `fn` to `λ.`)
  - Highlighting for `*.sig`, `*.fun`, `*.cm`, `*.mlb`, `*.lex`, `*.grm`, and
    `*.smackspec` files
- Indentation
  - Better `let ... in ... end` indentation
  - Better indentation with parentheses
- Filetype
  - Set up `'` and `$` as keyword characters
  - Set `'commentstring'` setting
- External plugins
  - delimitMate: set up quote characters
  - a.vim: set up `*.sig` and `*.sml` as alternates
  - Syntastic: detect and use CM files

## Usage

Most things work out of the box. **Some things require setup.**

Complete setup information is available in the help:

> [**`:help vim-better-sml`**](doc/vim-better-sml.txt).

Note: type introspection (`:SMLTypeQuery`) and unused variables requires that
MLton is installed. Unused variables and type error reporting require Syntastic.

## Configuration

A few settings are configurable. See `:help vim-better-sml-config`.

## Future Features

- [ ] Highlight all uses for a definition
  - Can probably do this with a quickfix window (think: vim-grepper)
- [ ] Handle non-standard mlton name/location
- [ ] Make it easier to get started porting CM to MLBasis
- [ ] Highlight all functions similar to vim-easytags
  - Might get this for free if we generate a tags file from the def-use
    information

## License

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](https://jez.io/MIT-LICENSE.txt)

<!-- References -->

[vim-ide]: https://github.com/jez/vim-as-an-ide
