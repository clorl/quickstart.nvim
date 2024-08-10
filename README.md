# quickstart.nvim [WIP]

Install neovim plugins, don't think about config, start working right away.
Quickstart is **not** a neovim distro, it's a collection of quickstart 
configurations for most popular neovim plugins.

Quickstart features a "from scratch" install so you can use it as a base for your
neovim config. Quickstart is also a plugin to allow you to easily download a 
quickstart config for any plugin and use it in your neovim config right away. It
features a plugin browser, quick usage documentation for plugins.

By default, quickstart is using lazy.nvim package manager.

# Installation

- Bootstrap script? Probably
- git clone but that omits the plugin part? I'd like to keep one repo for everything

# Usage (ideas)

Quickstart is both a config and a plugin, so that you can easily remove it
if you'd like.

You can also download the plugin on an existing neovim config.

```lua
{
    "nvim-telescope/telescope.nvim"
}
```

File structure
(But users can probably choose their own?)
```
~/.config/nvim/lua/
├── init.lua
├── plugins.lua
├── configs/
│   ├── lazy.lua
│   ├── telescope.lua
│   ├── lspconfig.lua
│   └── etc...
└── user | custom | whatever/
    └── configs/
        └── telescope.lua  -- Overrides the default
```

# Feature list

For the plugin part

- [ ] List/Picker for most popular nvim plugins (preconfigured)
    - [ ] Click and it adds it to your lazy.nvim plugins
    - [ ] Pull a plugin's config
- [ ] Plugin browser that shows neovim plugins from github (sorts available)
- [ ] Some kind of spec to easily list plugin extensions (telescope, cmp) or plugins recommended together (lspconfig and mason-lspconfig)
- [ ] Some kind of :qs contribute command that sends you to the issue/PR format to add a new config
- [ ] Should we have different presets for each plugin? Like "minimal", "recommended"

For the "distro" part

- [ ] :h qs.<plugin> gives you a basic overview of plugin usage, default keymaps etc. Also prompts you to check the plugin's actual config to know more
- [ ] Auto plugin config loading script like I have in my config

# Philosophy

- Single-file plugin list, one config file per plugin
- No abstraction on top of plugins
- No additional code layer, quickstart works just like a regular neovim config
- Modular, add and remove plugins effortlessly
- Opinionated defaults with documentation, so you can start using any plugin right away
- Choice, if you don't like one plugin's config, just make your own
- Invite plugins maintainers to contribute
