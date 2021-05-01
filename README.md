# rhacm-kustomization-app

We can use this repo to deploy RHACM via argo-cd application.
The app consists of both the operator and the instance.

* When combined, install runs very nice. However, when we go to uninstall,
  there are chances that the sub-component helm charts do not get uninstall properly. Most likely this is a timing issue, and the `- uninstall-helm-release` are not enough to block to cleanup of multiclusterhub or the csv.
