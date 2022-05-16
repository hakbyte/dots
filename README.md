# TODO

- [ ] Pyenv
- [ ] Update homedirs role to only delete empty folders (see https://www.reddit.com/r/ansible/comments/k9aqfq/remove_empty_dirs/)
- [ ] Create startup service or script to set sound output device on Desktop. Alternatively, set it via `/etc/pulse/default.pa`
- [ ] Add `.face` picture
- [ ] Install emoji extension () and set its keybinding to "<Super>." (default is "<Super>e")
- [ ] Zsh: make "" symbol from root prompt red
- [ ] Find way to programatically install Gnome extensions
- [ ] Configure Go path

# Notes

- Working with dconf commands:
  - Dump contents: `dconf dump /com/gexperts/Tilix/`
  - Clean up database for Tilix: `dconf list /com/gexperts/Tilix/ | xargs -I {} dconf reset -f "/com/gexperts/Tilix/"{}`
  - Watch for any changes: `dconf watch /` also `dconf watch /com/gexperts/Tilix/`
- Sound issue:
  - https://askubuntu.com/questions/1038490/how-do-you-set-a-default-audio-output-device-in-ubuntu/1207638#1207638
  - Commands:
    - pactl list short sinks                                                                                                          1 ⨯
    - pactl set-default-sink alsa_output.pci-0000_01_00.1.hdmi-stereo-extra2
