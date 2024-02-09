# ntbk / notebook - configure debian desktop with Ansible

Installs and configure the `.dotfiles` for:

- git
- gpg
- ssh
- zsh


## Install

```shell
$ sudo apt install ansible git ssh-client 
```


## Ansible vault password

```shell
$ mkdir -p ~/.config/ntbk/
$ echo ${NTBK_VAULT_PASSWORD} > ~/.config/ntbk/ansible-vault
```

_N.B. Vault password is in `Bitwarden`._


## Ansible pull

```shell
$ ansible-pull --url https://github.com/cvdg/ntbk.git
```


##

Afterwards:

- edit gpg trust `gpg --edit-key cees trust` to ultimate (ToDo)
- install `zsh` as primary shell
- install `tmux`
- install `neovim`
