# zsh-m365princess-prompt

A Powerline-style ZSH prompt theme inspired by [oh-my-posh M365Princess](https://ohmyposh.dev/docs/themes#m365princess).

## Features

- Colored segmented prompt bar with Powerline separators
- Time display with clock icon
- Shortened path display
- Git branch with icon (only shown in git repos)
- Two-line prompt with cursor on new line
- Clean right side (no RPROMPT)

## Color Palette

| Segment | Color | 256-color | Hex |
|---------|-------|-----------|-----|
| Time | Sky blue | 110 | #86BBD8 |
| Path | Blush/pink | 168 | #DA627D |
| Git | Salmon | 216 | #FCA17D |

## Requirements

This theme uses Powerline/Nerd Font unicode characters. Install a Nerd Font:

```bash
brew install font-meslo-lg-nerd-font
```

Then set your terminal font to "MesloLGM Nerd Font" (or similar).
- iTerm2: Settings → Profiles → Text → Font

## Installation

### With Prezto

1. Copy `prompt_skwp_custom_setup` to `~/.zprezto/modules/prompt/functions/`
2. Set in `~/.zpreztorc`:
   ```zsh
   zstyle ':prezto:module:prompt' theme 'skwp_custom'
   ```

### Manual

1. Add the file to a directory in your `$fpath`
2. Load with `autoload -Uz promptinit && promptinit && prompt skwp_custom`

## Preview

```
 10:30  ~/Code/project   main
$
```
