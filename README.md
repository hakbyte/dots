# TODO

- [x] Flameshot
- [ ] Pyenv
- [ ] Zsh
- [x] Tmux
- [ ] Homedirs
- [x] Tilix (including shortcuts + apperance -- all via dconf)
- [ ] GTK?

# Notes

- Remove background color of Neovim theme? May look better on Tilix
- Working with dconf commands:
  - Dump contents: `dconf dump /com/gexperts/Tilix/`
  - Clean up database for Tilix: `dconf list /com/gexperts/Tilix/ | xargs -I {} dconf reset -f "/com/gexperts/Tilix/"{}`
  - Watch for any changes: `dconf watch /` also `dconf watch /com/gexperts/Tilix/`
