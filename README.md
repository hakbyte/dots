# Dotfiles

My Kali Linux dotfiles, powered by [Ansible](https://www.ansible.com/).
Compared to other solutions I previously used to manage configuration files,
Ansible is way more flexible at the cost of _some_ complexity :)

Before running this playbook, install the dependencies:

```txt
sudo apt install ansible python3-psutil
```

# Usage

> :warning: Don't blindly run the playbook or your configuration files will
> be overwritten! If you're new to Ansible, run the playbooks in a VM and copy
> the tidbits that interest you. Otherwise spend some time to learn how
> everything fits together and adapt it to your environment.

```
$ git clone https://github.com/hakbyte/dots.git
$ cd dots
$ ansible-playbook -i hosts playbook.yml -e target=<TARGET>
```

> :memo: Possible values for `<TARGET>` are `desktop` or `laptop`. The former
> is fine tuned for a smaller screen (1920x1080 pixels) besides configuring the
> touchpad.

# Customization

You should check both `vars/all.yml` and `vars/pretasks.yml` for ways of customizing
this setup.

# TODO

- [ ] Update homedirs role to only delete empty folders (see https://www.reddit.com/r/ansible/comments/k9aqfq/remove_empty_dirs/)
- [ ] Change `.face` picture
- [ ] Install [Emoji Selector](https://extensions.gnome.org/extension/1162/emoji-selector/)
- [ ] Change Zsh's root prompt to red
- [ ] Add screenshot of current configuration
- [ ] Fix missing glyph in vim-airline
