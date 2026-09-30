# Modified CCXT 4.5.84 distribution for OHLC Bot

This repository holds an explicitly modified distribution of official CCXT v4.5.84 source commit `ec2f789b61dfaf647e4397f1bff31267e521ca72`. It is **not** an unchanged upstream release. The attached six-file patch updates dependency compatibility with react/http 1.11.1 and phpseclib 3.0.57. Original source and MIT license are preserved.

The GitHub Release archive is built by taking the official source ZIP for that commit and replacing only the six files named in `ccxt-v4.5.84-security.patch`. `distribution-manifest.json` records source, patch and archive SHA-256 hashes. Package consumers must pin the exact release archive and verify its checksum. No OHLC Bot application source, credentials or production data are included.

For future updates: inspect the latest stable official CCXT manifest first. If upstream supports safe dependency versions, return to the unmodified official package. Otherwise rebase and review this patch against the new exact stable source, retest lock installation, transport and Coinbase paths, then publish a new immutable artifact/version. Never silently repoint this release.
