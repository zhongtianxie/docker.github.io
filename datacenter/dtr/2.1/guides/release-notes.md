---
title: Docker Trusted Registry release notes
description: Docker Trusted Registry release notes
keywords:
- docker trusted registry, whats new, release notes
redirect_from:
- /docker-trusted-registry/release-notes/release-notes/
- /docker-trusted-registry/release-notes/
---

Here you can learn about new features, bug fixes, breaking changes and
known issues for each DTR version.

You can then use [the upgrade instructions](install/upgrade.md),
to upgrade your installation to the latest release.

## DTR 2.1

(10 Nov 2016)

**Features**

* Out of the box integration between UCP and DTR. You no longer need to
configure UCP to trust DTR and vice versa. Requires UCP 2.0 or higher
* DTR now contains its own Notary server you can use to store secure image
metadata
* Notary is highly-available if DTR is configured for high availability
* Added support of Google Cloud Storage driver using YML configurations
* Added support for Amazon S3 compatible storages like Cleversafe object store
by IBM

**Installer**

Made several improvements to the DTR installer, and added more configuration
flag, for more customization at install time.

* Several improvements to make installation more stable
* Added the `--log-tls-ca-cert`, `--log-tls-cert`, `--log-tls-key`,
`--log-tls-skip-verify` for specifying the TLS certificates to be used
with the DTR logging driver
* Added the `--enable-pprof` to enable pprof profiling of the server
* Added the `--etcd-heartbeat-interval`, `--etcd-election-timeout`, and
`--etcd-snapshot-count` options to configure the key-value store used by DTR
* Added the  `--nfs-storage-url`, and `--dtr-storage-volume` options to allow
configuring where Docker images are stored

**Web UI**

* Web UI now displays information about tag metadata and logs
* Improved garbage collection settings

**General improvements**

* Better integration with NFS storage driver to store Docker images
* Better integration with Filesystem storage driver to store Docker images
* Improved garbage collection performance and efficiency
* Improved health checking API for more granularity
