# Rustic K8S backup

This is a simple backup tool for Kubernetes persistent volumes (pv) using only Kustomize features.

It can scale resources to 0 before taking the backup and scale them back to the original state after the backup is done.

Example usage:

- [backup/kustomization.yml](./.github/testpv/backup/kustomization.yml) (once per (optional scalable resource) + pv).
- [forget/kustomization.yml](./.github/testpv/forget/kustomization.yml) (once per repository).
- To restore a backup, you need to specify a snapshot, review the [end to end test](./.github/workflows/e2e.yml).

