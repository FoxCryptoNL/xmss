<!--
    SPDX-FileCopyrightText: 2023 Fox Crypto B.V.
    SPDX-License-Identifier: CC-BY-4.0
-->

# XMSS

eXtended Merkle Signature Scheme is a post-quantum safe signature algorithm
([RFC](https://datatracker.ietf.org/doc/html/rfc8391)).

![XMSS C Library License](https://img.shields.io/github/license/FoxCryptoNL/xmss-library?style=plastic)
[![XMSS C Library Release](https://img.shields.io/github/v/release/FoxCryptoNL/xmss-library?style=plastic)](https://github.com/FoxCryptoNL/xmss-library/releases)

## XMSS C Library

This project contains a pure C99 implementation of the XMSS algorithm, developed by [Fox Crypto](https://foxcrypto.com).

The XMSS C library is production ready and is being maintained on premise to support evaluation at the highest possible
levels (e.g. Common Criteria). Please contact [Fox Crypto](https://foxcrypto.com) for details on how we can help getting
your product certified.

The library was developed under the Dutch "National Crypto Strategy" (NCS), aiming to speed up the development of first
class information security products, stimulating R&D in the crypto field, and strengthening collaboration between
government, companies and academia.

## Features

The library supports the 256-bits parameter sets recommended by
[NIST SP 800-208](https://csrc.nist.gov/publications/detail/sp/800-208/final):

- `XMSS-SHA2_10_256`
- `XMSS-SHA2_16_256`
- `XMSS-SHA2_20_256`
- `XMSS-SHAKE256_10_256`
- `XMSS-SHAKE256_16_256`
- `XMSS-SHAKE256_20_256`

Multi-tree XMSS (XMSS-MT) is not supported.

The library consists of two parts with slightly different, but complementary objectives.

### Signing

The signing part of the library delivers an API which includes not only the common signature operations, but also
provides solutions for availability, load balancing, and signature count hiding. It is optimized for use on modern PC or
server hardware.

### Verification

The verification library consists of a single C function which allows the caller to verify a signature against a payload
and a public key. It is optimized for resource-constrained hardware, including micro-controllers.

## Repositories

The XMSS C library is split over several repositories. This allows users to monitor the source code repository for
changes without having to deal with the more frequent updates to the documentation.

- Source code: [https://github.com/FoxCryptoNL/xmss-library](https://github.com/FoxCryptoNL/xmss-library)
- Documentation: [https://github.com/FoxCryptoNL/xmss-documentation](https://github.com/FoxCryptoNL/xmss-documentation)
