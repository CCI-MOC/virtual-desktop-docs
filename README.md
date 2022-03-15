# Shaw University Virtual Desktop @ Mass Open Cloud

We have deployed [Guacamole][], a web remote desktop gateway, on our [production OpenShift environment][ocp-prod]. You can find the deployment manifests in our [moc-apps][] repository in the [shaw-virtual-desktop][] directory. Manifests in the [`ocp-prod` overlay][ocp-prod overlay] are deployed using [ArgoCD][] and [Kustomize][]. Authentication services are provided by [Keycloak][].

We are creating virtual desktops using [OpenShift Virtualization][].

We have create some custom Python scripts to help manage Guacamole and automate the process of creating virtual machines; these are available in the [guac_py][] repository. The base image used for the virtual desktops was created using scripts from the [guac_vms][] repository.

[openshift virtualization]: https://cloud.redhat.com/learn/topics/virtualization/
[guacamole]: https://guacamole.apache.org/
[ocp-prod]: https://console-openshift-console.apps.ocp-prod.massopen.cloud/
[moc-apps]: https://github.com/CCI-MOC/moc-apps
[shaw-virtual-desktop]: https://github.com/CCI-MOC/moc-apps/tree/master/shaw-virtual-desktop
[ocp-prod overlay]: https://github.com/CCI-MOC/moc-apps/tree/master/shaw-virtual-desktop/overlays/ocp-prod
[argocd]: https://argo-cd.readthedocs.io/en/stable/
[kustomize]: https://kustomize.io/
[guac_py]: https://github.com/larsks/guac_py
[guac_vms]: https://github.com/larsks/guac_vms
[keycloak]: https://www.keycloak.org/
