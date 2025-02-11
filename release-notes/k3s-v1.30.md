| k3s version| Kubernetes | Kine | SQLite | Etcd | Containerd | Runc | Flannel | Metrics-server | Traefik | CoreDNS | Helm-controller | Local-path-provisioner  |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | -----  |
| v1.30.2+k3s1 | [v1.30.2](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.30.md#v1302) | [v0.11.9](https://github.com/k3s-io/kine/releases/tag/v0.11.9) | [3.44.0](https://sqlite.org/releaselog/3_44_0.html) | [v3.5.13-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.13-k3s1) | [v1.7.17-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.17-k3s1) | [v1.1.12](https://github.com/opencontainers/runc/releases/tag/v1.1.12) | [v0.25.2](https://github.com/flannel-io/flannel/releases/tag/v0.25.2) | [v0.7.0](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.7.0) | [v2.10.7](https://github.com/traefik/traefik/releases/tag/v2.10.7) | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | [v0.16.1](https://github.com/k3s-io/helm-controller/releases/tag/v0.16.1) | [v0.0.27](https://github.com/rancher/local-path-provisioner/releases/tag/v0.0.27)  |
| v1.30.1+k3s1 | [v1.30.1](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.30.md#v1301) | [v0.11.8-0.20240430184817-f9ce6f8da97b](https://github.com/k3s-io/kine/releases/tag/v0.11.8-0.20240430184817-f9ce6f8da97b) | [3.44.0](https://sqlite.org/releaselog/3_44_0.html) | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1) | [v1.7.15-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.15-k3s1) | [v1.1.12-k3s1](https://github.com/opencontainers/runc/releases/tag/v1.1.12-k3s1) | [v0.24.2](https://github.com/flannel-io/flannel/releases/tag/v0.24.2) | [v0.7.0](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.7.0) | [v2.10.7](https://github.com/traefik/traefik/releases/tag/v2.10.7) | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | [v0.16.1-0.20240502205943-2f32059d43e6](https://github.com/k3s-io/helm-controller/releases/tag/v0.16.1-0.20240502205943-2f32059d43e6) | [v0.0.26](https://github.com/rancher/local-path-provisioner/releases/tag/v0.0.26)  |
| v1.30.0+k3s1 | [v1.30.0](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.30.md#v1300) | [v0.11.8](https://github.com/k3s-io/kine/releases/tag/v0.11.7) | [3.44.0](https://sqlite.org/releaselog/3_44_0.html) | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1) | [v1.7.15-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.15-k3s1) | [v1.1.12](https://github.com/opencontainers/runc/releases/tag/v1.1.12) | [v0.24.2](https://github.com/flannel-io/flannel/releases/tag/v0.24.2) | [v0.7.0](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.7.0) | [v2.10.7](https://github.com/traefik/traefik/releases/tag/v2.10.7) | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | [v0.16.1](https://github.com/k3s-io/helm-controller/releases/tag/v0.15.9) | [v0.0.26](https://github.com/rancher/local-path-provisioner/releases/tag/v0.0.26)  |



| Version | Release date | US date | EU date | Upstream release date | US date | EU date | Days since upstream |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| [v1.30.2+k3s1](k3s-v1.30.md#release-v1302k3s1) | Jun 25 2024 | 06/25/24 | 2024-06-25 | Jun 12 2024 | 06/12/24 | 2024-06-12 | 13 days |
| [v1.30.1+k3s1](k3s-v1.30.md#release-v1301k3s1) | May 22 2024 | 05/22/24 | 2024-05-22 | May 15 2024 | 05/15/24 | 2024-05-15 | 7 days |
| [v1.30.0+k3s1](k3s-v1.30.md#release-v1300k3s1) | May 10 2024 | 05/10/24 | 2024-05-10 | Apr 17 2024 | 04/17/24 | 2024-04-17 | 23 days |



# Release v1.30.2+k3s1
<!-- v1.30.2+k3s1 -->

This release updates Kubernetes to v1.30.2, and fixes a number of issues.

For more details on what's new, see the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.30.md#changelog-since-v1301).

## Changes since v1.30.1+k3s1:

* Fix bug when using tailscale config by file [(#10074)](https://github.com/k3s-io/k3s/pull/10074)
  * Fix bug when using `vpn-auth-file` in the agent
* Add WithSkipMissing to not fail import on missing blobs [(#10136)](https://github.com/k3s-io/k3s/pull/10136)
* Use fixed stream server bind address for cri-dockerd [(#9975)](https://github.com/k3s-io/k3s/pull/9975)
* Switch stargz over to cri registry config_path [(#9977)](https://github.com/k3s-io/k3s/pull/9977)
* Bump to containerd v1.7.17, etcd v3.5.13 [(#10123)](https://github.com/k3s-io/k3s/pull/10123)
* Bump spegel version [(#10118)](https://github.com/k3s-io/k3s/pull/10118)
* Fix issue installing artifacts from PR builds with multiple runs [(#10122)](https://github.com/k3s-io/k3s/pull/10122)
* Fix issue with `externalTrafficPolicy: Local` for single-stack services on dual-stack nodes [(#9963)](https://github.com/k3s-io/k3s/pull/9963)
* Update local-path-provisioner helper script [(#9964)](https://github.com/k3s-io/k3s/pull/9964)
* Add support for svclb pod PriorityClassName [(#10045)](https://github.com/k3s-io/k3s/pull/10045)
  * ServiceLB now sets the priorityClassName on svclb pods to `system-node-critical` by default. This can be overridden on a per-service basis via the `svccontroller.k3s.cattle.io/priorityclassname` annotation.
* Drop check for legacy traefik v1 chart [(#9593)](https://github.com/k3s-io/k3s/pull/9593)
  * K3s no longer automatically skips deploying traefik v2 if traefik v1 is present. All clusters should have been upgraded to v2 at some point over the last three years.
* Update kube-router version to v2.1.2 [(#10177)](https://github.com/k3s-io/k3s/pull/10177)
* Create ADR for branching strategy [(#10147)](https://github.com/k3s-io/k3s/pull/10147)
* Bump minio-go to v7.0.70 [(#10081)](https://github.com/k3s-io/k3s/pull/10081)
* Bump kine to v0.11.9 to fix pagination [(#10082)](https://github.com/k3s-io/k3s/pull/10082)
* Update valid resolv conf [(#9948)](https://github.com/k3s-io/k3s/pull/9948)
* Add missing kernel config check [(#10100)](https://github.com/k3s-io/k3s/pull/10100)
* Git workflow file name correction [(#10131)](https://github.com/k3s-io/k3s/pull/10131)
  * None
* Follow directory symlinks in auto deploying manifests (#9288) [(#10049)](https://github.com/k3s-io/k3s/pull/10049)
  * Symlinked sub-directories are now respected when scanning Auto-Deploying Manifests (AddOns)
* Fix bug: allow helm controller set owner reference [(#10048)](https://github.com/k3s-io/k3s/pull/10048)
* Fix go.mod [(#10192)](https://github.com/k3s-io/k3s/pull/10192)
* Bump flannel version to v0.25.2 [(#10146)](https://github.com/k3s-io/k3s/pull/10146)
* Test: add agent with auth file [(#10119)](https://github.com/k3s-io/k3s/pull/10119)
  * Fix bug when using `vpn-auth-file` in the agent
* Add extra log in e2e tests [(#10145)](https://github.com/k3s-io/k3s/pull/10145)
* Update channel server for may 2024 [(#10137)](https://github.com/k3s-io/k3s/pull/10137)
* Bump klipper-helm image for tls secret support [(#10187)](https://github.com/k3s-io/k3s/pull/10187)
* Updating the script binary_size_check to complete the command name by… [(#9992)](https://github.com/k3s-io/k3s/pull/9992)
* Fix issue with k3s-etcd informers not starting [(#10047)](https://github.com/k3s-io/k3s/pull/10047)
* Enable serving supervisor metrics [(#10019)](https://github.com/k3s-io/k3s/pull/10019)
  * `--Enable-pprof` can now be set on agents to enable the debug/pprof endpoints. When set, agents will listen on the supervisor port.
  * `--Supervisor-metrics` can now be set on servers to enable serving internal metrics on the supervisor endpoint; when set agents will listen on the supervisor port.
* Bump alpine from 3.18 to 3.20 in /conformance [(#10210)](https://github.com/k3s-io/k3s/pull/10210)
* Bump alpine from 3.18 to 3.20 in /package [(#10211)](https://github.com/k3s-io/k3s/pull/10211)
* Bump ubuntu from 22.04 to 24.04 in /tests/e2e/scripts [(#10040)](https://github.com/k3s-io/k3s/pull/10040)
* Bump Trivy version [(#10039)](https://github.com/k3s-io/k3s/pull/10039)
* Fix netpol crash when node remains tained unintialized [(#10073)](https://github.com/k3s-io/k3s/pull/10073)
* Fix issue caused by sole server marked as failed under load [(#10241)](https://github.com/k3s-io/k3s/pull/10241)
  * The embedded load-balancer will now fall back to trying all servers with health-checks ignored, if all servers have been marked unavailable due to failed health checks.
* Add write-kubeconfig-group flag to server [(#9233)](https://github.com/k3s-io/k3s/pull/9233)
  * New flag in k3s server: --write-kubeconfig-group
* Fix embedded mirror blocked by SAR RBAC and re-enable test [(#10257)](https://github.com/k3s-io/k3s/pull/10257)
* Bump Local Path Provisioner version [(#10268)](https://github.com/k3s-io/k3s/pull/10268)
* Fix: Use actual warningPeriod in certmonitor [(#10271)](https://github.com/k3s-io/k3s/pull/10271)
* Fix bug that caused agents to bypass local loadbalancer [(#10280)](https://github.com/k3s-io/k3s/pull/10280)
* Add ADR for support for etcd s3 config secret [(#9364)](https://github.com/k3s-io/k3s/pull/9364)
* Add test for `isValidResolvConf` [(#10302)](https://github.com/k3s-io/k3s/pull/10302)
* Add snapshot retention etcd-s3-folder fix [(#10293)](https://github.com/k3s-io/k3s/pull/10293)
* Expand GHA golang caching to includ newest release branch [(#10307)](https://github.com/k3s-io/k3s/pull/10307)
* Fix race condition panic in loadbalancer.nextServer [(#10318)](https://github.com/k3s-io/k3s/pull/10318)
* Fix typo, use `rancher/permissions` [(#10296)](https://github.com/k3s-io/k3s/pull/10296)
* Update Kubernetes to v1.30.2 [(#10349)](https://github.com/k3s-io/k3s/pull/10349)
* Fix agent supervisor port using apiserver port instead [(#10352)](https://github.com/k3s-io/k3s/pull/10352)
* Fix issue that allowed multiple simultaneous snapshots to be allowed [(#10372)](https://github.com/k3s-io/k3s/pull/10372)

## Embedded Component Versions
| Component | Version |
|---|---|
| Kubernetes | [v1.30.2](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.30.md#v1302) |
| Kine | [v0.11.9](https://github.com/k3s-io/kine/releases/tag/v0.11.9) |
| SQLite | [3.44.0](https://sqlite.org/releaselog/3_44_0.html) |
| Etcd | [v3.5.13-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.13-k3s1) |
| Containerd | [v1.7.17-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.17-k3s1) |
| Runc | [v1.1.12](https://github.com/opencontainers/runc/releases/tag/v1.1.12) |
| Flannel | [v0.25.2](https://github.com/flannel-io/flannel/releases/tag/v0.25.2) | 
| Metrics-server | [v0.7.0](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.7.0) |
| Traefik | [v2.10.7](https://github.com/traefik/traefik/releases/tag/v2.10.7) |
| CoreDNS | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | 
| Helm-controller | [v0.16.1](https://github.com/k3s-io/helm-controller/releases/tag/v0.16.1) |
| Local-path-provisioner | [v0.0.27](https://github.com/rancher/local-path-provisioner/releases/tag/v0.0.27) |

## Helpful Links
As always, we welcome and appreciate feedback from our community of users. Please feel free to:
- [Open issues here](https://github.com/rancher/k3s/issues/new/choose)
- [Join our Slack channel](https://slack.rancher.io/)
- [Check out our documentation](https://rancher.com/docs/k3s/latest/en/) for guidance on how to get started or to dive deep into K3s.
- [Read how you can contribute here](https://github.com/rancher/k3s/blob/master/CONTRIBUTING.md)

-----
# Release v1.30.1+k3s1
<!-- v1.30.1+k3s1 -->

This release updates Kubernetes to v1.30.1, and fixes a number of issues.

For more details on what's new, see the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.30.md#changelog-since-v1300).

## Changes since v1.30.0+k3s1:

* Replace deprecated ruby function in e2e tests [(#10084)](https://github.com/k3s-io/k3s/pull/10084)
* Update channels with 1.30 [(#10097)](https://github.com/k3s-io/k3s/pull/10097)
* Address 461 [(#10112)](https://github.com/k3s-io/k3s/pull/10112)
* Update to v1.30.1-k3s1 and Go 1.22.2 [(#10105)](https://github.com/k3s-io/k3s/pull/10105)

## Embedded Component Versions
| Component | Version |
|---|---|
| Kubernetes | [v1.30.1](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.30.md#v1301) |
| Kine | [v0.11.8-0.20240430184817-f9ce6f8da97b](https://github.com/k3s-io/kine/releases/tag/v0.11.8-0.20240430184817-f9ce6f8da97b) |
| SQLite | [3.44.0](https://sqlite.org/releaselog/3_44_0.html) |
| Etcd | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1) |
| Containerd | [v1.7.15-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.15-k3s1) |
| Runc | [v1.1.12-k3s1](https://github.com/opencontainers/runc/releases/tag/v1.1.12-k3s1) |
| Flannel | [v0.24.2](https://github.com/flannel-io/flannel/releases/tag/v0.24.2) | 
| Metrics-server | [v0.7.0](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.7.0) |
| Traefik | [v2.10.7](https://github.com/traefik/traefik/releases/tag/v2.10.7) |
| CoreDNS | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | 
| Helm-controller | [v0.16.1-0.20240502205943-2f32059d43e6](https://github.com/k3s-io/helm-controller/releases/tag/v0.16.1-0.20240502205943-2f32059d43e6) |
| Local-path-provisioner | [v0.0.26](https://github.com/rancher/local-path-provisioner/releases/tag/v0.0.26) |

## Helpful Links
As always, we welcome and appreciate feedback from our community of users. Please feel free to:
- [Open issues here](https://github.com/rancher/k3s/issues/new/choose)
- [Join our Slack channel](https://slack.rancher.io/)
- [Check out our documentation](https://rancher.com/docs/k3s/latest/en/) for guidance on how to get started or to dive deep into K3s.
- [Read how you can contribute here](https://github.com/rancher/k3s/blob/master/CONTRIBUTING.md)


## What's Changed
* Replace deprecated ruby function in e2e tests by @manuelbuil in https://github.com/k3s-io/k3s/pull/10084
* Update channels with 1.30 by @galal-hussein in https://github.com/k3s-io/k3s/pull/10097
* Address 461 by @HarrisonWAffel in https://github.com/k3s-io/k3s/pull/10112
* Update to v1.30.1-k3s1 and Go 1.22.2 by @briandowns in https://github.com/k3s-io/k3s/pull/10105


**Full Changelog**: https://github.com/k3s-io/k3s/compare/v1.30.0+k3s1...v1.30.1+k3s1
-----
# Release v1.30.0+k3s1
<!-- v1.30.0+k3s1 -->


This release is K3S's first in the v1.30 line. This release updates Kubernetes to v1.30.0.

For more details on what's new, see the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.30.md#changelog-since-v1290).

## Changes since v1.29.4+k3s1:

* Kubernetes V1.30.0-k3s1 [(#10063)](https://github.com/k3s-io/k3s/pull/10063)
* Update stable channel to v1.29.4+k3s1 [(#10031)](https://github.com/k3s-io/k3s/pull/10031)
* Add E2E Split Server to Drone, support parallel testing in Drone [(#9940)](https://github.com/k3s-io/k3s/pull/9940)
* Bump E2E opensuse leap to 15.6, fix btrfs test [(#10057)](https://github.com/k3s-io/k3s/pull/10057)
* Remove deprecated `pod-infra-container-image` kubelet flag [(#7409)](https://github.com/k3s-io/k3s/pull/7409)
* Fix e2e tests [(#10061)](https://github.com/k3s-io/k3s/pull/10061)


## Embedded Component Versions
| Component | Version |
|---|---|
| Kubernetes | [v1.30.0](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.30.md#v1300) |
| Kine | [v0.11.8](https://github.com/k3s-io/kine/releases/tag/v0.11.7) |
| SQLite | [3.44.0](https://sqlite.org/releaselog/3_44_0.html) |
| Etcd | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1) |
| Containerd | [v1.7.15-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.15-k3s1) |
| Runc | [v1.1.12](https://github.com/opencontainers/runc/releases/tag/v1.1.12) |
| Flannel | [v0.24.2](https://github.com/flannel-io/flannel/releases/tag/v0.24.2) | 
| Metrics-server | [v0.7.0](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.7.0) |
| Traefik | [v2.10.7](https://github.com/traefik/traefik/releases/tag/v2.10.7) |
| CoreDNS | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | 
| Helm-controller | [v0.16.1](https://github.com/k3s-io/helm-controller/releases/tag/v0.15.9) |
| Local-path-provisioner | [v0.0.26](https://github.com/rancher/local-path-provisioner/releases/tag/v0.0.26) |

## Helpful Links
As always, we welcome and appreciate feedback from our community of users. Please feel free to:
- [Open issues here](https://github.com/rancher/k3s/issues/new/choose)
- [Join our Slack channel](https://slack.rancher.io/)
- [Check out our documentation](https://rancher.com/docs/k3s/latest/en/) for guidance on how to get started or to dive deep into K3s.
- [Read how you can contribute here](https://github.com/rancher/k3s/blob/master/CONTRIBUTING.md)
-----
