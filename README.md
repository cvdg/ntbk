# ntbk / notebook - configure debian desktop with Ansible

Installs and configure the `.dotfiles` for:

- git
- gpg
- nvim
- ssh
- tmux
- zsh


## Pre-install

```shell
$ sudo apt install ansible git ssh-client 
```


### Ansible vault password

```shell
$ mkdir -p ~/.config/ntbk/
$ echo ${NTBK_VAULT_PASSWORD} > ~/.config/ntbk/ansible-vault
```

_N.B. Vault password is in `Bitwarden`._


## Install: ansible pull

```shell
$ ansible-pull --url https://github.com/cvdg/ntbk.git
```


## Post-install:

```shell
$ ansible-pull --ask-become-password --url https://github.com/cvdg/ntbk.git install.yml
```

- edit gpg trust `gpg --edit-key cees trust` to ultimate (ToDo)
- install `zsh` as primary shell: `chsh -s /usr/bin/zsh`

The `nvim` version in Debian stable (Bookworm) is very old and does not work with `LazyVim`.
