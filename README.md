# datastar-lsp

Language server for [Datastar](https://data-star.dev) hypermedia framework.

## Features

- **Diagnostics** - unknown attributes, missing keys/values, undefined signals/actions, invalid modifiers
- **Hover** - per-part docs for plugin name, key, modifier, and value (e.g. `data-signals__ifmissing` shows modifier description)
- **Completions** - `$` signals, `@` actions, `data-` attributes, `:` keys, `__` modifiers, event types
- **Go-to-definition** - `$signal` to `data-signals:signal` across all indexed files
- **Find references** - all `$signal` usages across the workspace
- **Rename** - rename a signal everywhere (camelCase/kebab-case aware)
- **Code actions** - quick-fix to define undefined signals, add missing values/keys

## Supported Languages

HTML · Templ (Go) · JSX · TSX · HEEx (Elixir) · Blade (PHP)

## Install

### Neovim (lazy.nvim)

```lua
{
    "hyperpuncher/datastar-lsp",
    opts = {},
}
```

### VS Code

Download `datastar-lsp-*.vsix` from the [latest release](https://github.com/hyperpuncher/datastar-lsp/releases/latest), then:

```bash
code --install-extension datastar-lsp-*.vsix
```

### Zed

```bash
git clone https://github.com/hyperpuncher/datastar-lsp
```

Then in Zed, run `zed: install dev extension` and select the `datastar-lsp/zed/` directory.

## Requirements

- [tree-sitter-datastar](https://github.com/hyperpuncher/tree-sitter-datastar) for syntax highlighting (optional but recommended)
