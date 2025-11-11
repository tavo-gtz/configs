# Configs

This repository contains the config files I use to customize my terminal environment. These files help me maintain a consistent setup across different machines and save time when setting up new environments.

![screenshot](/demo.png)

## Essential Tools

- **Starship**: [Customizable prompt for any shell](https://starship.rs/) 
- **Eza**: [Command line utility that makes 'ls' more user-friendly](https://github.com/eza-community/eza) 

## Setup

#### Prerequisites
- A nerd font installed and enabled in your terminal.

#### Installation

1. Install latest versions using brew.

```bash
brew install starship
brew install eza
```

2. Add the init script and custom path for config files to the end of `.zshrc`.

```
nano ~/.zshrc
```

```
#Starship
export STARSHIP_CONFIG="$HOME/Dev/configs/starship/starship.toml"
eval "$(starship init zsh)"

#Eza
export EZA_CONFIG_DIR="$HOME/Dev/configs/eza"
```

3. Add the alias for ls command.
```
#Custom aliases
alias ls='eza --icons --group-directories-first'
```

## Uninstalling

To remove starship prompt or eza simply use brew to uninstall.
```bash
brew uninstall starship
```

```
brew uninstall eza
```
Then open your shell's configuration file (e.g., ~/.zshrc). Locate and delete all lines related to the package you want to delete.
