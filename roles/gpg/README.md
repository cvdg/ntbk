## Gpg

Import public and secret key.

```shell
$ cd ~/.gnupg
$ gpg --import cees-pub.txt
gpg: key 11E965F14AB03635: "Cees van de Griend <cees.van.de.griend@protonmail.com>" not changed
gpg: Total number processed: 1
gpg:              unchanged: 1
$ gpg --import cees-sec.txt
gpg: key 11E965F14AB03635: "Cees van de Griend <cees.van.de.griend@protonmail.com>" not changed
gpg: key 11E965F14AB03635: secret key imported
gpg: Total number processed: 1
gpg:              unchanged: 1
gpg:       secret keys read: 1
gpg:  secret keys unchanged: 1
```

Set the trust to ultimate.

```shell
$ gpg --edit-key cees trust
gpg (GnuPG) 2.2.40; Copyright (C) 2022 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Secret key is available.

sec  ed25519/11E965F14AB03635
     created: 2023-10-02  expires: 2026-10-01  usage: SC
     trust: ultimate      validity: ultimate
ssb  cv25519/ED2FE5C3D300AA64
     created: 2023-10-02  expires: 2026-10-01  usage: E
[ultimate] (1). Cees van de Griend <cees.van.de.griend@protonmail.com>

sec  ed25519/11E965F14AB03635
     created: 2023-10-02  expires: 2026-10-01  usage: SC
     trust: ultimate      validity: ultimate
ssb  cv25519/ED2FE5C3D300AA64
     created: 2023-10-02  expires: 2026-10-01  usage: E
[ultimate] (1). Cees van de Griend <cees.van.de.griend@protonmail.com>

Please decide how far you trust this user to correctly verify other users' keys
(by looking at passports, checking fingerprints from different sources, etc.)

  1 = I don't know or won't say
  2 = I do NOT trust
  3 = I trust marginally
  4 = I trust fully
  5 = I trust ultimately
  m = back to the main menu

Your decision? 5
Do you really want to set this key to ultimate trust? (y/N) y

sec  ed25519/11E965F14AB03635
     created: 2023-10-02  expires: 2026-10-01  usage: SC
     trust: ultimate      validity: ultimate
ssb  cv25519/ED2FE5C3D300AA64
     created: 2023-10-02  expires: 2026-10-01  usage: E
[ultimate] (1). Cees van de Griend <cees.van.de.griend@protonmail.com>

gpg> quit
```


Apend to `~/.bashrc`:

```
export GPG_TTY=$(tty)
```
