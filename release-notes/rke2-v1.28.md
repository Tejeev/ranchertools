| RKE2 version| Kubernetes | Etcd | Containerd | Runc | Metrics-server | CoreDNS | Ingress-Nginx | Helm-controller | Canal (Default) | Calico | Cilium | Multus  |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | -----  |
| v1.28.3+rke2r1 | [v1.28.3](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.28.md#v1283) | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1) | [v1.7.7-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.7-k3s1) | [v1.1.8](https://github.com/opencontainers/runc/releases/tag/v1.1.8) | [v0.6.3](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.6.3) | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | [4.8.2](https://github.com/kubernetes/ingress-nginx/releases/tag/helm-chart-4.8.2) | [v0.15.4](https://github.com/k3s-io/helm-controller/releases/tag/v0.15.4) | [Flannel v0.22.1](https://github.com/flannel-io/flannel/releases/tag/v0.22.1)<br/>[Calico v3.26.1](https://docs.tigera.io/calico/latest/release-notes/#v3.26) | [v3.26.1](https://docs.tigera.io/calico/latest/release-notes/#v3.26) | [v1.14.2](https://github.com/cilium/cilium/releases/tag/v1.14.2) | [v4.0.2](https://github.com/k8snetworkplumbingwg/multus-cni/releases/tag/v4.0.2)  |
| v1.28.2+rke2r1 | [v1.28.2](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.28.md#v1282) | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1) | [v1.7.3-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.3-k3s1) | [v1.1.8](https://github.com/opencontainers/runc/releases/tag/v1.1.8) | [v0.6.3](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.6.3) | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1) | [4.6.1](https://github.com/kubernetes/ingress-nginx/releases/tag/helm-chart-4.6.1) | [v0.15.4](https://github.com/k3s-io/helm-controller/releases/tag/v0.15.4) | [Flannel v0.22.1](https://github.com/flannel-io/flannel/releases/tag/v0.22.1)<br/>[Calico v3.26.1](https://docs.tigera.io/calico/latest/release-notes/#v3.26) | [v3.26.1](https://docs.tigera.io/calico/latest/release-notes/#v3.26) | [v1.14.1](https://github.com/cilium/cilium/releases/tag/v1.14.1) | [v4.0.2](https://github.com/k8snetworkplumbingwg/multus-cni/releases/tag/v4.0.2)  |



| Version | Release date | US date | EU date | Upstream release date | US date | EU date | Days since upstream |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| [v1.28.3+rke2r1](rke2-v1.28.md#release-v1283rke2r1) | Oct 31 2023 | 10/31/23 | 2023-10-31 | Oct 18 2023 | 10/18/23 | 2023-10-18 | 13 days |
| [v1.28.2+rke2r1](rke2-v1.28.md#release-v1282rke2r1) | Sep 18 2023 | 09/18/23 | 2023-09-18 | Sep 13 2023 | 09/13/23 | 2023-09-13 | 5 days |



# Release v1.28.3+rke2r1
<!-- v1.28.3+rke2r1 -->

This release updates Kubernetes to v1.28.3.

**Important Notes**

This release includes a version of ingress-nginx affected by [CVE-2023-5043](https://github.com/kubernetes/ingress-nginx/issues/10571) and [CVE-2023-5044](https://github.com/kubernetes/ingress-nginx/issues/10572). Ingress administrators should set the --enable-annotation-validation flag to enforce restrictions on the contents of ingress-nginx annotation fields.

If your server (control-plane) nodes were not started with the `--token` CLI flag or config file key, a randomized token was generated during initial cluster startup. This key is used both for joining new nodes to the cluster, and for encrypting cluster bootstrap data within the datastore. Ensure that you retain a copy of this token, as is required when restoring from backup.

You may retrieve the token value from any server already joined to the cluster:
```bash
cat /var/lib/rancher/rke2/server/token
```

## Changes since v1.28.2+rke2r1:

* Add a time.Sleep in calico-win to avoid polluting the logs [(#4723)](https://github.com/rancher/rke2/pull/4723)
* Update stable channel to v1.26.9 [(#4774)](https://github.com/rancher/rke2/pull/4774)
* Bump actions/checkout from 3 to 4 [(#4746)](https://github.com/rancher/rke2/pull/4746)
* Fix .github regex to skip drone runs on gh action bumps [(#4800)](https://github.com/rancher/rke2/pull/4800)
* Add skip fapolicy option [(#4673)](https://github.com/rancher/rke2/pull/4673)
* Update calico chart to accept felix config values [(#4802)](https://github.com/rancher/rke2/pull/4802)
* Handle restart attempts in static pod manifest checks [(#4784)](https://github.com/rancher/rke2/pull/4784)
  * Fixed an issue where static pod startup checks may return false positives in the case of pod restarts
* Remove unnecessary docker pull [(#4820)](https://github.com/rancher/rke2/pull/4820)
* Update charts to have ipFamilyPolicy: PreferDualStack as default [(#4780)](https://github.com/rancher/rke2/pull/4780)
  * Use ipFamilyPolicy: PreferDualStack for system services: coredns, metrics-server, nginx and snapshot-validation-webhook
* Mirrored pause update [(#4829)](https://github.com/rancher/rke2/pull/4829)
* Fix function name on comment [(#4668)](https://github.com/rancher/rke2/pull/4668)
* Fix slemicro check for selinux [(#4830)](https://github.com/rancher/rke2/pull/4830)
* Write pod-manifests as 0600 in cis mode [(#4831)](https://github.com/rancher/rke2/pull/4831)
* Filter to not accept dependabot and updatecli branchs [(#4841)](https://github.com/rancher/rke2/pull/4841)
* Bump k3s version in go.mod [(#4850)](https://github.com/rancher/rke2/pull/4850)
* Bump cilium to 1.14.2 [(#4837)](https://github.com/rancher/rke2/pull/4837)
* Bump K3s, Token Rotation support [(#4866)](https://github.com/rancher/rke2/pull/4866)
* Bump containerd to v1.7.7+k3s1 [(#4879)](https://github.com/rancher/rke2/pull/4879)
* Remove SECURITY.md [(#4868)](https://github.com/rancher/rke2/pull/4868)
* Bump K3s version for v1.28 [(#4883)](https://github.com/rancher/rke2/pull/4883)
  * RKE2 now tracks snapshots using custom resource definitions. This resolves an issue where the configmap previously used to track snapshot metadata could grow excessively large and fail to update when new snapshots were taken.
* Bump dependencies [(#4865)](https://github.com/rancher/rke2/pull/4865)
* Bump k3s [(#4896)](https://github.com/rancher/rke2/pull/4896)
* Bump rke2-cloud-controller to v1.28.2-build20231016 [(#4895)](https://github.com/rancher/rke2/pull/4895)
* Bump K3s version for v1.28 [(#4916)](https://github.com/rancher/rke2/pull/4916)
  * Re-enable etcd endpoint auto-sync 
  * Manually requeue configmap reconcile when no nodes have reconciled snapshots
* Update Kubernetes to v1.28.3 [(#4923)](https://github.com/rancher/rke2/pull/4923)
* Fix: upgrading Go in go.mod to 1.20 [(#4911)](https://github.com/rancher/rke2/pull/4911)
* Remove pod-manifests dir in killall script [(#4929)](https://github.com/rancher/rke2/pull/4929)
* Bump ingress-nginx to v1.9.3 [(#4955)](https://github.com/rancher/rke2/pull/4955)
* Bump K3s version for v1.28 [(#4968)](https://github.com/rancher/rke2/pull/4968)

## Packaged Component Versions
| Component       | Version                                                                                           |
| --------------- | ------------------------------------------------------------------------------------------------- |
| Kubernetes      | [v1.28.3](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.28.md#v1283) |
| Etcd            | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1)                            |
| Containerd      | [v1.7.7-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.7-k3s1)                      |
| Runc            | [v1.1.8](https://github.com/opencontainers/runc/releases/tag/v1.1.8)                              |
| Metrics-server  | [v0.6.3](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.6.3)                   |
| CoreDNS         | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1)                                |
| Ingress-Nginx   | [4.8.2](https://github.com/kubernetes/ingress-nginx/releases/tag/helm-chart-4.8.2)                |
| Helm-controller | [v0.15.4](https://github.com/k3s-io/helm-controller/releases/tag/v0.15.4)                         |

### Available CNIs
| Component       | Version                                                                                                                                                   | FIPS Compliant |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- |
| Canal (Default) | [Flannel v0.22.1](https://github.com/flannel-io/flannel/releases/tag/v0.22.1)<br/>[Calico v3.26.1](https://docs.tigera.io/calico/latest/release-notes/#v3.26) | Yes            |
| Calico          | [v3.26.1](https://docs.tigera.io/calico/latest/release-notes/#v3.26)                                                                                      | No             |
| Cilium          | [v1.14.2](https://github.com/cilium/cilium/releases/tag/v1.14.2)                                                                                          | No             |
| Multus          | [v4.0.2](https://github.com/k8snetworkplumbingwg/multus-cni/releases/tag/v4.0.2)                                                                          | No             |

## Helpful Links

As always, we welcome and appreciate feedback from our community of users. Please feel free to:
- [Open issues here](https://github.com/rancher/rke2/issues/new)
- [Join our Slack channel](https://slack.rancher.io/)
- [Check out our documentation](https://docs.rke2.io) for guidance on how to get started.
-----
# Release v1.28.2+rke2r1
<!-- v1.28.2+rke2r1 -->

This release updates Kubernetes to v1.28.2.

**Important Note**

If your server (control-plane) nodes were not started with the `--token` CLI flag or config file key, a randomized token was generated during initial cluster startup. This key is used both for joining new nodes to the cluster, and for encrypting cluster bootstrap data within the datastore. Ensure that you retain a copy of this token, as is required when restoring from backup.

You may retrieve the token value from any server already joined to the cluster:
```bash
cat /var/lib/rancher/rke2/server/token
```

## Changes since v1.28.1+rke2r1:

* Support new generic "cis" profile [(#4708)](https://github.com/rancher/rke2/pull/4708)
* Update cilium to 1.14.1 [(#4755)](https://github.com/rancher/rke2/pull/4755)
* Update Kubernetes to v1.28.2 Go to v1.20.8 [(#4760)](https://github.com/rancher/rke2/pull/4760)

## Packaged Component Versions
| Component       | Version                                                                                           |
| --------------- | ------------------------------------------------------------------------------------------------- |
| Kubernetes      | [v1.28.2](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.28.md#v1282) |
| Etcd            | [v3.5.9-k3s1](https://github.com/k3s-io/etcd/releases/tag/v3.5.9-k3s1)                            |
| Containerd      | [v1.7.3-k3s1](https://github.com/k3s-io/containerd/releases/tag/v1.7.3-k3s1)                      |
| Runc            | [v1.1.8](https://github.com/opencontainers/runc/releases/tag/v1.1.8)                              |
| Metrics-server  | [v0.6.3](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.6.3)                   |
| CoreDNS         | [v1.10.1](https://github.com/coredns/coredns/releases/tag/v1.10.1)                                |
| Ingress-Nginx   | [4.6.1](https://github.com/kubernetes/ingress-nginx/releases/tag/helm-chart-4.6.1)                |
| Helm-controller | [v0.15.4](https://github.com/k3s-io/helm-controller/releases/tag/v0.15.4)                         |

### Available CNIs
| Component       | Version                                                                                                                                                   | FIPS Compliant |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------- |
| Canal (Default) | [Flannel v0.22.1](https://github.com/flannel-io/flannel/releases/tag/v0.22.1)<br/>[Calico v3.26.1](https://docs.tigera.io/calico/latest/release-notes/#v3.26) | Yes            |
| Calico          | [v3.26.1](https://docs.tigera.io/calico/latest/release-notes/#v3.26)                                                                                      | No             |
| Cilium          | [v1.14.1](https://github.com/cilium/cilium/releases/tag/v1.14.1)                                                                                          | No             |
| Multus          | [v4.0.2](https://github.com/k8snetworkplumbingwg/multus-cni/releases/tag/v4.0.2)                                                                          | No             |

## Helpful Links

As always, we welcome and appreciate feedback from our community of users. Please feel free to:
- [Open issues here](https://github.com/rancher/rke2/issues/new)
- [Join our Slack channel](https://slack.rancher.io/)
- [Check out our documentation](https://docs.rke2.io) for guidance on how to get started.
-----
