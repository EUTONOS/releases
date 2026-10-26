# EUTONOS releases

This repository publishes signed EUTONOS releases. The source code is kept elsewhere; only release files appear here,
under [Releases](../../releases).

Each release carries three files:

- the EUTONOS package (`.whl`);
- `eutonos-release.json`, which names the version and the package's sha256;
- `eutonos-release.json.sig`, an Ed25519 signature over that file.

An installed EUTONOS checks this repository for new versions. Before anything is installed it verifies the signature
against the release key built into EUTONOS and checks the package against the signed sha256. A release that fails either
check is refused, and the version already installed stays active.

No license is granted for the files published here; all rights are reserved.
