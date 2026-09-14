# camargo.nvim

Colorscheme para Neovim baseado nos três temas de leitura de [gustavocamargo.com](https://gustavocamargo.com/): escuro, sépia e claro.

## Instalação (LazyVim)

```lua
-- lua/plugins/colorscheme.lua
return {
  { "gcamargosilva/lazy-camargo", lazy = false, priority = 1000 },
  { "LazyVim/LazyVim", opts = { colorscheme = "camargo" } },
}
```

Sem LazyVim:

```lua
{
  "gcamargosilva/lazy-camargo",
  lazy = false,
  priority = 1000,
  config = function()
    vim.cmd.colorscheme("camargo")
  end,
}
```

## Variantes

A variante segue `background`:

| `background` | Variante | Fundo     | Texto     | Accent    |
| ------------ | -------- | --------- | --------- | --------- |
| `dark`       | escuro   | `#17181b` | `#cfcac2` | `#c59c6d` |
| `light`      | sépia    | `#e8e6dd` | `#252525` | `#884b35` |
| `light`      | claro    | `#faf9f7` | `#1c1b19` | `#32618e` |

`<leader>ub` no LazyVim (ou `:set background=light`) alterna. Para usar o claro no lugar do sépia, antes de carregar o colorscheme:

```lua
vim.g.camargo_light = "claro"
```

## Cobertura

Treesitter, LSP, diagnósticos, diff, gitsigns, snacks, blink.cmp, which-key, flash, noice, mini.icons, render-markdown, mason e cores do terminal.
