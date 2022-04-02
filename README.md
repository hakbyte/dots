# TODO

- [x] Flameshot
- [ ] Pyenv
- [ ] Zsh
- [x] Tmux
- [x] Homedirs: how to deal with defaults in Files app?
- [x] Tilix (including shortcuts + apperance -- all via dconf)
- [ ] GTK: shrink titlebars (see eog app)?
- [x] Also change appearance of gnome terminal (default from Kali with Gnome DE)
- [ ] Add shortcut to launch a regular terminal (maybe Tilix, maybe Gnome terminal)
- [ ] Find out how to customize Nautilus folder's under "Recent"
- [ ] Update homedirs role to only delete empty folders (see https://www.reddit.com/r/ansible/comments/k9aqfq/remove_empty_dirs/)
- [ ] Create startup service or script to set sound output device on Desktop. Alternatively, set it via `/etc/pulse/default.pa`

# Notes

- Remove background color of Neovim theme? May look better on Tilix
- Working with dconf commands:
  - Dump contents: `dconf dump /com/gexperts/Tilix/`
  - Clean up database for Tilix: `dconf list /com/gexperts/Tilix/ | xargs -I {} dconf reset -f "/com/gexperts/Tilix/"{}`
  - Watch for any changes: `dconf watch /` also `dconf watch /com/gexperts/Tilix/`
- Sound issue:
  - https://askubuntu.com/questions/1038490/how-do-you-set-a-default-audio-output-device-in-ubuntu/1207638#1207638
  - Commands:
    - pactl list short sinks                                                                                                          1 ⨯
    - pactl set-default-sink alsa_output.pci-0000_01_00.1.hdmi-stereo-extra2
