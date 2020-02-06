---
description: 'https://wiki.polkadot.network/docs/en/learn-cryptography'
---

# Cryptography Overview

### Hashing Algorithm

The hashing algorithm used in Edgeware and Substrate is [Blake2b](https://en.wikipedia.org/wiki/BLAKE_%28hash_function%29#BLAKE2). Blake2 is considered to be a very fast cryptographic hash function that is also used in the cryptocurrency [Zcash](https://z.cash/).

### Keypairs and Signing

Edgeware uses Schnorrkel/Ristretto x25519 \("sr25519"\) as its key derivation and signing algorithm.

Sr25519 is based on the same underlying [Curve25519](https://en.wikipedia.org/wiki/Curve25519) as its EdDSA counterpart, [Ed25519](https://en.wikipedia.org/wiki/EdDSA#Ed25519). However, it uses Schnorr signatures instead of the EdDSA scheme. Schnorr signatures bring some noticeable benefits over the ECDSA/EdDSA schemes. For one, it is more efficient and still retains the same feature set and security assumptions. Additionally, it allows for native multisignature through [signature aggregation](https://bitcoincore.org/en/2017/03/23/schnorr-signature-aggregation/).

The names Schnorrkel and Ristretto come from the two Rust libraries that implement this scheme, the [Schnorrkel](https://github.com/w3f/schnorrkel) library for Schnorr signatures and the [Ristretto](https://ristretto.group/ristretto.html) library that makes it possible to use cofactor-8 curves like Curve25519.

{% page-ref page="account-keys.md" %}


