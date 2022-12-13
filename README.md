# lazy.nvim

## ✨ Features

## ✅ TODO

- [x] fancy UI to manage all your Neovim plugins
- [x] auto lazy-loading of lua modules
- [x] lazy-loading on events, commands, filetypes and key mappings
- [x] Partial clones instead of shallow clones
- [x] waits till missing deps are installed (bootstrap Neovim and start using it right away)
- [x] Async
- [x] No need to manually compile
- [x] Fast. Automatically caches and compiles byte code of all lua modules needed during startup
- [x] Correct sequencing of dependencies (deps should always be opt. Maybe make everything opt?)
- [x] Config in multiple files
- [x] dev option and patterns for local packages
- [x] Profiling
- [x] lockfile `lazy-lock.json`
- [x] upvalues in `config` & `init`
- [x] check for updates
- [x] commit, branch, tag, version support
- [x] semver https://devhints.io/semver
- [x] auto-loading on completion for lazy-loaded commands
- [x] bootstrap code
- [x] Background update checker
- [x] statusline component to see number of pending updates
- [x] health checks: check merge conflicts async
  - [x] unsupported props or props from other managers
  - [x] other packages still in site?
  - [x] other package manager artifacts still present? compiled etc
- [x] status page showing running handlers and cache stats
- [x] temp colorscheme used during startup when installing missing plugins
- [x] automatically reloads when config changes are detected
- [x] handlers imply opt
- [x] dependencies imply opt for deps
- [ ] show spec errors in health
- [ ] fix plugin details
- [ ] show disabled plugins (strikethrough?)
- [ ] log file
- [ ] git tests
- [ ] Import specs from other plugin managers
- [ ] [packspec](https://github.com/nvim-lua/nvim-package-specification)
  - [ ] add support to specify `engines`, `os` and `cpu` like in `package.json`
  - [ ] semver merging. Should check if two or more semver ranges are compatible and calculate the union range
    - default semver merging strategy: if no version matches all, then use highest version?
  - [ ] package meta index (package.lua cache for all packages)

## 📦 Differences with Packer

- **Plugin Spec**:

  - `setup` => `init`
  - `requires` => `dependencies`
  - `as` => `name`
  - `opt` => `lazy`
  - `run` => `build`
  - `lock` => `pin`
  - `module` is auto-loaded. No need to specify

## 📦 Other Neovim Plugin Managers in Lua

- [packer.nvim](https://github.com/wbthomason/packer.nvim)
- [paq-nvim](https://github.com/savq/paq-nvim)
- [neopm](https://github.com/ii14/neopm)
- [dep](https://github.com/chiyadev/dep)
- [optpack.nvim](https://github.com/notomo/optpack.nvim)
- [pact.nvim](https://github.com/rktjmp/pact.nvim)
