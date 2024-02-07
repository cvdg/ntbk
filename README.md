# ntbk / notebook - configure debian desktop with Ansible


## Install

```shell
$ sudo apt install ssh-client git python3 ansible
```


## Ansible vault password


```shell
$ mkdir -p ~/.config/ntbk/
$ echo $NTBK_VAULT_PASSWORD > ~/.config/ntbk/ansible-vault
```

_N.B. Vault password is in `Bitwarden`._


## Ansible pull

```shell
$ ansible-pull --ask-become-pass --url https://github.com/cvdg/ntbk.git
```


## Git sign with Gpg

```
$  gpg --list-secret-keys --keyid-format=long
/home/cees/.gnupg/pubring.kbx
-----------------------------
sec   ed25519/11E965F14AB03635 2023-10-02 [SC] [expires: 2026-10-01]
      5C7C70F2263A7C7FD1C8663D11E965F14AB03635
uid                 [ultimate] Cees van de Griend <cees.van.de.griend@protonmail.com>
ssb   cv25519/ED2FE5C3D300AA64 2023-10-02 [E] [expires: 2026-10-01]

$ git config --global user.signingkey 11E965F14AB03635
$ git config --global commit.gpgsign true
```
