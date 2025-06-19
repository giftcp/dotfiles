# Dotfiles

This repository contains my personal Linux dotfiles, organized for easy deployment and version control across systems. The setup is tailored for a Wayland environment using the Hyprland compositor, with a focus on performance, minimalism, and productivity.

## Features

- **Shell Configurations**: Customizations for both `bash` and `zsh` shells.
- **Window Manager**: Configuration for Hyprland under `hypr/`.
- **Terminal Emulator**: Themed and optimized `kitty` terminal configuration.
- **Editor**: Full Neovim setup under `nvim/`, utilizing modern plugins and performance tweaks.
- **System Bar**: A Waybar configuration with CPU and memory widgets added.
- **Launcher**: `wofi` setup, including a custom configuration adapted from TypeScript.
- **Kubernetes**: `.kube` directory maintained at the root level for cluster configuration files.

## Repository Structure
.
├── .bashrc # Bash shell configuration
├── .zshrc # Zsh shell configuration
├── .gitignore # Ignore rules for backup/system-specific files
├── README.md # This file
└── .config/
├── hypr/ # Hyprland window manager settings
├── kitty/ # Kitty terminal configuration
├── nvim/ # Neovim configuration and plugin management
├── waybar/ # Waybar status bar settings
└── wofi/ # Wofi launcher configuration

## Setup Instructions

To deploy these dotfiles on a new system:

1. Clone the repository:

```bash
git clone https://github.com/yourusername/dotfiles.git ~/dotfiles
```

2. Create symbolic links or copy the files to your home directory:

```bash
ln -s ~/dotfiles/.bashrc ~/.bashrc
ln -s ~/dotfiles/.zshrc ~/.zshrc
ln -s ~/dotfiles/.config/hypr ~/.config/hypr
ln -s ~/dotfiles/.config/kitty ~/.config/kitty
ln -s ~/dotfiles/.config/nvim ~/.config/nvim
ln -s ~/dotfiles/.config/waybar ~/.config/waybar
ln -s ~/dotfiles/.config/wofi ~/.config/wofi
ln -s ~/dotfiles/.kube ~/.kube
Reload your shell or reboot to apply changes.
```
3. Reload your shell or reboot to apply changes.


## Notes
Ensure all required dependencies (such as hyprland, kitty, neovim, waybar, and wofi) are installed.

These dotfiles assume a Linux environment using Wayland; behavior may vary on other setups.
