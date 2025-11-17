# My Neovim 
This configuration is focused on being fast, minimal, and pretty!
It was originally based on [kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim), but has divereged quiet a lot since then.

## Overview
The config is using `lazy.nvim` as a plugin manager, `mason.nvim` for lsp and `nvim-treesitter` for syntax highlighting.   
<img width="2560" height="1440" alt="nvim_peek" src="https://github.com/user-attachments/assets/e18ed0e1-6ecf-49a1-8fbe-5709498db3c9" />

## Plugins
All plugins managed by `lazy` are under [lua/plugins/](lua/plugins/). The most important ones are: 
- `nvim-lspconfig` -> for lsp
- `conform.nvim` -> for auto formatting
- `blink.cmp` -> auto completion
- `nvim-treesitter` -> syntax highlighting 
- `mini.nvim` -> using `mini.ai`, `mini.surround` and `mini.splitjoin`
- `colorbuddy.nvim` -> for custom color sheme
- `telescope` -> fuzzy finder for files, grep, diagnositcs, code actions/definitions/references/diagnostics... (mots under `\<leader\>f` or `\<leader\>c`)
- `which-key.nvim` -> keymap help
- `yazi.nvim` -> explorer 

## Color theme
The custom color theme is under [/colors/gruvbuddy.lua](/colors/gruvbuddy.lua) and uses the theme switching from my [arch sytem](https://github.com/Atrejooo/arch_dotfiles) via the `@@color_name@@` annotations.\
The transparency is controlled under [/lua/core/transparent.lua](/lua/core/transparent.lua) and can be turned on or off (for systems/terminals that allow transparent window backgrounds).

## Tabline
The tabline is self made and it's lua code is under [lua/core/tabliny.lua](lua/core/tabliny.lua). 
It uses the custom color themes colors and displays: 
- buffernames
- modified, waring and error markers as M W or E
- highlights selected buffer

## All custom keymaps
Most (except lsp related) custom keymaps can be found under [lua/core/keymaps.lua](lua/core/keymaps.lua). The most important ones are: 
- `\<leader\>f` for all find commands using telescope
- `\<leader\>c` all code and lsp related actions
- `\<leader\>e` open yazi
- `\<leader\>/` fuzzy find in current buffer
- `\<leader\>t` toggles comments, tabline and line wrapping
- `H` next buffer to the left
- `L` next buffer to the right
