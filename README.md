# PowerDarwin Roots

Apple's builds of the Darwin 9 projects, the Roots of Mac OS X Leopard's builds 9A581 (10.5) to 9L30 (10.5.8), each with its source, kept for [PowerDarwin](https://github.com/nyg/PowerDarwin), which builds Darwin 9 for PowerPC Macs and starts its builds from these Roots.

## Where they come from

Apple published the Roots for darwinbuild at `src.macosforge.org/Roots/<build>/`. That server is gone. These files were downloaded from the Wayback Machine, which serves them from ArchiveBot's crawl of src.macosforge.org of 23 February 2014, and are unchanged: each has the SHA-256 that PowerDarwin's [manifest/9L30-roots.sha256](https://github.com/nyg/PowerDarwin/blob/master/manifest/9L30-roots.sha256) records.

The sources are Apple's tarballs, unchanged: from each project's tag in [apple-oss-distributions](https://github.com/apple-oss-distributions) on GitHub, or, for the versions GitHub lacks, from the Wayback Machine's copy of `www.opensource.apple.com/tarballs/`. [sources.tsv](sources.tsv) gives the address of each.

## Releases

- [roots-9L30](https://github.com/nyg/PowerDarwin-roots/releases/tag/roots-9L30): 524 Roots, 1.04 GB. Each is named after its build and its file: `9L30_xnu.root.tar.gz` is `src.macosforge.org/Roots/9L30/xnu.root.tar.gz`.
- [sources-9L30](https://github.com/nyg/PowerDarwin-roots/releases/tag/sources-9L30): 364 source tarballs, 1.00 GB: the source of each Root, at the version that Root was built from, and SQLite 46.1, which PowerDarwin builds.

[roots.tsv](roots.tsv) lists each Root with its original address, size, SHA-256, project, version, source tarball and licence, and [sources.tsv](sources.tsv) each source tarball with its size, SHA-256, address and licence. [roots.sha256](roots.sha256) and [sources.sha256](sources.sha256) check a download: `shasum -a 256 -c roots.sha256` in the folder that holds the downloaded Roots.

## Licences

Each Root is Apple's build of one Darwin project and is under that project's licence. For 491 of the 524 Roots, [roots.tsv](roots.tsv) gives the licence that Apple's release pages for Mac OS X 10.5 to 10.5.8 on opensource.apple.com gave for that project and version, with the names those pages used: `apsl`, `bsd`, `gpl` and so on. For the other 33, it gives the licences that the source of that version states. Most of Apple's own projects are under the Apple Public Source License, and the others under the GPL, the LGPL, BSD, MIT, Apache, MPL, CDDL, Artistic, Sleepycat, IBM Public License and other licences.

The source of every Root is in the sources-9L30 release, at the version that Root was built from. So no Root is distributed in executable form only, and each one's source is offered from the same place as the Root, as the APSL, the GPL, the LGPL, the MPL, the CDDL, the IBM Public License and the Sleepycat licence ask. Each source tarball holds its project's licence texts and notices. [LICENSES/](LICENSES/) holds the APSL 1.0, 1.1 and 2.0, the GPL 2.0 and the LGPL 2.0 and 2.1, copied unchanged from Apple's tarballs of architecture 254.0.5, IOFireWireFamily 344.4.0, IOATAPIProtocolTransport 152.0.1, bc 21, cxxfilt 7 and gcc 5465.

Six of the 530 Roots that PowerDarwin uses are not here, as nothing puts them under an open-source licence: CarbonHeaders 9G55 (Root and headers), AppleDisplays 1151.0.0 and AppleUSBAudio 264.2.17 (Root and headers), whose source Apple never published, and security_certificates 36946, whose source states no licence. PowerDarwin downloads those from the Wayback Machine.

This product includes software developed by the OpenSSL Project for use in the OpenSSL Toolkit (http://www.openssl.org/), and cryptographic software written by Eric Young (eay@cryptsoft.com).

Apple, Mac OS X and Darwin are trademarks of Apple Inc. This repository is not made, approved or supported by Apple.

This README, the lists and the checksum files are under the MIT licence, Copyright (c) 2026 nyg, as PowerDarwin's own files are.
