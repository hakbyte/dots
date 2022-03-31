# TODO

- [x] Flameshot
- [ ] Pyenv
- [ ] Zsh
- [x] Tmux
- [ ] Homedirs: how to deal with defaults in Files app?
- [x] Tilix (including shortcuts + apperance -- all via dconf)
- [ ] GTK: shrink titlebars (see eog app)?
- [x] Also change appearance of gnome terminal (default from Kali with Gnome DE)
- [ ] Add shortcut to launch a regular terminal (maybe Tilix, maybe Gnome terminal)

# Notes

- Remove background color of Neovim theme? May look better on Tilix
- Working with dconf commands:
  - Dump contents: `dconf dump /com/gexperts/Tilix/`
  - Clean up database for Tilix: `dconf list /com/gexperts/Tilix/ | xargs -I {} dconf reset -f "/com/gexperts/Tilix/"{}`
  - Watch for any changes: `dconf watch /` also `dconf watch /com/gexperts/Tilix/`
