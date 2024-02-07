# ntbk / notebook - configure debian desktop with Ansible


## Install

```shell
$ sudo apt install ssh-client git gnupg2 python3 ansible
```


## Ansible vault password


```shell
$ mkdir -p ~/.config/ntbk/
$ echo ${NTBK_VAULT_PASSWORD} > ~/.config/ntbk/ansible-vault
```

_N.B. Vault password is in `Bitwarden`._


## Ansible pull

```shell
$ ansible-pull --ask-become-pass --url https://github.com/cvdg/ntbk.git
```
