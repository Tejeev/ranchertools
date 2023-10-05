| k3s version| Kubernetes | Kine | SQLite | Etcd | Containerd | Runc | Flannel | Metrics-server | Traefik | CoreDNS | Helm-controller | Local-path-provisioner  |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | -----  |
| v1.28.2+k3s1 | [v1.28.2](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.28.md#v1282) | [v0.10.3](https://github.com/k3s-io/kine/releases/tag/v0.10.3) | [3.42.0](https://sqlite.org/releaselog/3_42_0.html) | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1) | [v1.7.6-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.6-k3s1) | [v1.1.8](https://github.com/opencontainers/runc/releases/tag/v1.1.8) | [v0.22.2](https://github.com/flannel-io/flannel/releases/tag/v0.22.2) | [v0.6.3](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.6.3) | [v2.9.10](https://github.com/traefik/traefik/releases/tag/v2.9.10) | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | [v0.15.4](https://github.com/k3s-io/helm-controller/releases/tag/v0.15.4) | [v0.0.24](https://github.com/rancher/local-path-provisioner/releases/tag/v0.0.24)  |
| v1.28.1+k3s1 | [v1.28.1](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.28.md#v1281) | [v0.10.3](https://github.com/k3s-io/kine/releases/tag/v0.10.3) | [3.42.0](https://sqlite.org/releaselog/3_42_0.html) | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1) | [v1.7.3-k3s2](https://github.com/k3s-io/containerd/releases/tag/v1.7.3-k3s2) | [v1.1.8](https://github.com/opencontainers/runc/releases/tag/v1.1.8) | [v0.22.2](https://github.com/flannel-io/flannel/releases/tag/v0.22.2) | [v0.6.3](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.6.3) | [v2.9.10](https://github.com/traefik/traefik/releases/tag/v2.9.10) | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | [v0.15.4](https://github.com/k3s-io/helm-controller/releases/tag/v0.15.4) | [v0.0.24](https://github.com/rancher/local-path-provisioner/releases/tag/v0.0.24)  |



| Version | Release date | US date | EU date | Upstream release date | US date | EU date | Days since upstream |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| [v1.28.2+k3s1](k3s-v1.28.md#release-v1282k3s1) | Sep 20 2023 | 09/20/23 | 2023-09-20 | Sep 13 2023 | 09/13/23 | 2023-09-13 | 7 days |
| [v1.28.1+k3s1](k3s-v1.28.md#release-v1281k3s1) | Sep 08 2023 | 09/08/23 | 2023-09-08 | Aug 24 2023 | 08/24/23 | 2023-08-24 | 15 days |



# Release v1.28.2+k3s1
<!-- v1.28.2+k3s1 -->

This release updates Kubernetes to v1.28.2, and fixes a number of issues.

For more details on what's new, see the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.28.md#changelog-since-v1281).

## Changes since v1.28.1+k3s1:

* Update channel for version v1.28 [(#8305)](https://github.com/k3s-io/k3s/pull/8305)
* Bump kine to v0.10.3 [(#8323)](https://github.com/k3s-io/k3s/pull/8323)
* Update to v1.28.2 and go v1.20.8 [(#8364)](https://github.com/k3s-io/k3s/pull/8364)
  * Bump embedded containerd to v1.7.6
  * Bump embedded stargz-snapshotter plugin to latest
  * Fixed intermittent drone CI failures due to race conditions in test environment setup scripts
  * Fixed CI failures due to changes to api discovery changes in Kubernetes 1.28

## Embedded Component Versions
| Component | Version |
|---|---|
| Kubernetes | [v1.28.2](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.28.md#v1282) |
| Kine | [v0.10.3](https://github.com/k3s-io/kine/releases/tag/v0.10.3) |
| SQLite | [3.42.0](https://sqlite.org/releaselog/3_42_0.html) |
| Etcd | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1) |
| Containerd | [v1.7.6-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.6-k3s1) |
| Runc | [v1.1.8](https://github.com/opencontainers/runc/releases/tag/v1.1.8) |
| Flannel | [v0.22.2](https://github.com/flannel-io/flannel/releases/tag/v0.22.2) | 
| Metrics-server | [v0.6.3](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.6.3) |
| Traefik | [v2.9.10](https://github.com/traefik/traefik/releases/tag/v2.9.10) |
| CoreDNS | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | 
| Helm-controller | [v0.15.4](https://github.com/k3s-io/helm-controller/releases/tag/v0.15.4) |
| Local-path-provisioner | [v0.0.24](https://github.com/rancher/local-path-provisioner/releases/tag/v0.0.24) |

## Helpful Links
As always, we welcome and appreciate feedback from our community of users. Please feel free to:
- [Open issues here](https://github.com/rancher/k3s/issues/new/choose)
- [Join our Slack channel](https://slack.rancher.io/)
- [Check out our documentation](https://rancher.com/docs/k3s/latest/en/) for guidance on how to get started or to dive deep into K3s.
- [Read how you can contribute here](https://github.com/rancher/k3s/blob/master/CONTRIBUTING.md)

-----
# Release v1.28.1+k3s1
<!-- v1.28.1+k3s1 -->
This release is K3S's first in the v1.28 line. This release updates Kubernetes to v1.28.1.

⚠️ IMPORTANT: This release includes remediation for CVE-2023-32187, a potential Denial of Service attack vector on K3s servers. See https://github.com/k3s-io/k3s/security/advisories/GHSA-m4hf-6vgr-75r2 for more information, including documentation on changes in behavior that harden clusters against this vulnerability.

Kubernetes v1.28 contains a critical regression ([kubernetes/kubernetes#120247](https://github.com/kubernetes/kubernetes/issues/120247)) that causes init containers to run at the same time as app containers following a restart of the node. This issue will be fixed in v1.28.2. We do not recommend using K3s v1.28 at this time if your application depends on init containers.

For more details on what's new, see the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.28.md#changelog-since-v1270).

## Changes since v1.27.5+k3s1:

* Update to v1.28.1 [(#8239)](https://github.com/k3s-io/k3s/pull/8239)
* CLI Removal for v1.28.0 [(#8203)](https://github.com/k3s-io/k3s/pull/8203)
* Secrets Encryption V3 [(#8111)](https://github.com/k3s-io/k3s/pull/8111)
* Add new CLI flag to disable TLS SAN CN filtering [(#8252)](https://github.com/k3s-io/k3s/pull/8252)
  * Added a new `--tls-san-security` option.
* Add RWMutex to address controller [(#8268)](https://github.com/k3s-io/k3s/pull/8268)

## Embedded Component Versions
| Component | Version |
|---|---|
| Kubernetes | [v1.28.1](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.28.md#v1281) |
| Kine | [v0.10.3](https://github.com/k3s-io/kine/releases/tag/v0.10.3) |
| SQLite | [3.42.0](https://sqlite.org/releaselog/3_42_0.html) |
| Etcd | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1) |
| Containerd | [v1.7.3-k3s2](https://github.com/k3s-io/containerd/releases/tag/v1.7.3-k3s2) |
| Runc | [v1.1.8](https://github.com/opencontainers/runc/releases/tag/v1.1.8) |
| Flannel | [v0.22.2](https://github.com/flannel-io/flannel/releases/tag/v0.22.2) | 
| Metrics-server | [v0.6.3](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.6.3) |
| Traefik | [v2.9.10](https://github.com/traefik/traefik/releases/tag/v2.9.10) |
| CoreDNS | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | 
| Helm-controller | [v0.15.4](https://github.com/k3s-io/helm-controller/releases/tag/v0.15.4) |
| Local-path-provisioner | [v0.0.24](https://github.com/rancher/local-path-provisioner/releases/tag/v0.0.24) |

## Helpful Links
As always, we welcome and appreciate feedback from our community of users. Please feel free to:
- [Open issues here](https://github.com/rancher/k3s/issues/new/choose)
- [Join our Slack channel](https://slack.rancher.io/)
- [Check out our documentation](https://rancher.com/docs/k3s/latest/en/) for guidance on how to get started or to dive deep into K3s.
- [Read how you can contribute here](https://github.com/rancher/k3s/blob/master/CONTRIBUTING.md)
-----