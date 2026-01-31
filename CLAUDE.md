# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a ZSH prompt theme inspired by [oh-my-posh M365Princess](https://ohmyposh.dev/docs/themes#m365princess). It provides a Powerline-style segmented prompt with:
- Path segment (blush/pink, 256-color: 168)
- Git branch segment (salmon, 256-color: 216) - only shown in git repos
- Time segment (sky blue, 256-color: 110)
- Two-line prompt with cursor on second line

## File Structure

- `prompt_skwp_custom_setup` - The complete ZSH prompt theme (single file)

## Installation

The theme follows the Prezto prompt naming convention (`prompt_<name>_setup`). To use:
1. Place `prompt_skwp_custom_setup` in a directory in your `$fpath`
2. Run `prompt skwp_custom` or add to `.zpreztorc`

## Requirements

Requires a Nerd Font for proper Powerline character display:
```bash
brew install font-meslo-lg-nerd-font
```

## Architecture

The prompt uses a segment-based drawing system:
- `prompt_segment <bg> <fg> <content>` - Draws a segment with color transition
- `prompt_end` - Closes the prompt line with final separator
- `prompt_dir`, `prompt_git`, `prompt_time` - Individual segment builders
- `prompt_main` - Orchestrates segment drawing
- `prompt_skwp_custom_setup` - Entry point following Prezto conventions

The `CURRENT_BG` variable tracks the previous segment's background color to draw proper Powerline transitions between segments.

## Testing Changes

Source the file directly to test:
```zsh
source prompt_skwp_custom_setup
```
