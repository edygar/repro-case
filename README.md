# [Issue #63](https://github.com/rachartier/tiny-code-action.nvim/issues/63)

This repo serves to help on investigating the [issue #63](https://github.com/rachartier/tiny-code-action.nvim/issues/63)
of the awesome plugin https://github.com/rachartier/tiny-code-action.nvim

## Reproduce steps

I've used AstroNVIM to speed up the setup, so hopefully it will be straight forward:

```sh
git clone --depth 1 https://github.com/edygar/repro-case ~/.config/repro-case
cd ~/.config/repro-case/
NVIM_APPNAME=repro-case nvim main.ts
```

>> I had to close and reopen `NVIM_APPNAME=repro-case nvim main.ts` after the plugins/treesitter/lsp installations

Now, press <code>lrA</code> (capital A), this is the standard AstroNVIM for displaying
code actions with the only from `source` and empty diagnostics.

I couldn't do the same with tiny-code-action.

```nvim
lua require("tiny-code-action").code_action({ filters = { kind = "source" } })

```
