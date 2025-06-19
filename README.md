# Dotfiles

This repository contains my personal Linux dotfiles, structured for use with [GNU Stow](https://www.gnu.org/software/stow/) to simplify the management and deployment of configuration files across systems.

The configuration is optimized for a Wayland-based environment using the **Hyprland** compositor, and includes setups for terminal, editor, bar, launcher, and shells.

## Features

- **Shells**: `.bashrc` and `.zshrc` for bash and zsh customizations.
- **Hyprland**: Window manager configuration under `hypr/`.
- **Kitty**: A clean, fast terminal with settings stored in `kitty/`.
- **Neovim**: Complete IDE setup via `nvim/` using modern plugin management.
- **Waybar**: System bar enhancements including CPU and memory widgets.
- **Wofi**: Application launcher configured using TypeScript-based styles.
- **Stow-Ready**: All folders are organized to allow seamless use with GNU Stow.

## Directory Layout

```
.
├── bashrc/                 # Contains .bashrc
├── zshrc/                  # Contains .zshrc
├── gitignore/              # Contains .gitignore
├── hypr/                   # Contains .config/hypr
├── kitty/                  # Contains .config/kitty
├── nvim/                   # Contains .config/nvim
├── waybar/                 # Contains .config/waybar
├── wofi/                   # Contains .config/wofi
└── README.md               # This file
```

> Note: Each top-level directory is structured so that Stow can symlink files into `$HOME`.

## Usage with GNU Stow

1. Clone the repository into your home directory or a central dotfiles directory:

   ```bash
   git clone https://github.com/yourusername/dotfiles.git ~/dotfiles
   cd ~/dotfiles
   ```

2. Stow the desired configuration(s):

   ```bash
   stow bashrc
   stow zshrc
   stow hypr
   stow kitty
   stow nvim
   stow waybar
   stow wofi
   stow kube
   stow gitignore
   ```

   This will symlink the relevant files and folders into your `$HOME` directory. For example, `bashrc/.bashrc` will be linked to `~/.bashrc`.

## Notes

- Ensure all necessary packages (e.g. `hyprland`, `kitty`, `neovim`, `waybar`, `wofi`, `stow`) are installed.
- These dotfiles are designed for Wayland compositors and may not work as intended in X11 environments.

## License

These dotfiles are distributed under the MIT License. Feel free to use, fork, or modify them to suit your workflow.
