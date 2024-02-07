# Git sign

```shell
$ gpg --list-secret-keys --keyid-format=long
/home/cees/.gnupg/pubring.kbx
-----------------------------
sec   ed25519/11E965F14AB03635 2023-10-02 [SC] [expires: 2026-10-01]
      5C7C70F2263A7C7FD1C8663D11E965F14AB03635
uid                 [ultimate] Cees van de Griend <cees.van.de.griend@protonmail.com>
ssb   cv25519/ED2FE5C3D300AA64 2023-10-02 [E] [expires: 2026-10-01]

$ git config --global user.signingkey 11E965F14AB03635
$ git config --global commit.gpgsign true
```
