# gh-actions-lsp.nvim 

![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/ellisonleao/nvim-plugin-template/lint-test.yml?branch=main&style=for-the-badge)
![Lua](https://img.shields.io/badge/Made%20with%20Lua-blueviolet.svg?style=for-the-badge&logo=lua)

A Neovim plugin that integrates with the GitHub Actions Language Server to provide LSP features for GitHub workflow files.

## Prerequisites

This plugin requires the `gh-actions-language-server` binary to be installed. You can install it via npm:

```bash
npm install -g @github/gh-actions-language-server
```

## Installation

### Lazy.nvim

Add the following to your Lazy.nvim configuration:

```lua
{
  "tamerlang/gh-actions-lsp.nvim",
  opts = {}
}
```

Or with custom configuration:

```lua
{
  "tamerlang/gh-actions-lsp.nvim",
  opts = {
    -- Add any custom options here
  },
  ft = { "yaml" }, -- Only load for YAML files
  event = "VeryLazy" -- Or load on specific events
}
```

### Manual Installation

If you prefer manual installation, clone this repository to your Neovim configuration directory:

```bash
git clone https://github.com/tamerlang/gh-actions-lsp.nvim ~/.config/nvim/pack/plugins/start/gh-actions-lsp.nvim
```

Then add the plugin to your configuration:

```lua
require("gh-actions-lsp").setup({})
```

## Usage

The plugin automatically detects GitHub workflow files (`.github/workflows/*.yml` and `.github/workflows/*.yaml`) and attaches the Language Server when you open them.

## Configuration

The plugin uses sensible defaults, but you can customize its behavior:

```lua
require("gh-actions-lsp").setup({
  -- Configuration options will be documented here as they're added
})
```

