# K8S simple backup

A simple backup solution for Kubernetes Persistent Volumes (pv) using only [Kustomize](https://kustomize.io/) features.

It can optionally scale resources to 0 before taking the backup and scale them back to the original state after the
backup is done.

The project defaults to a borg backup/restore, but this and everything else can be easily changed using kustomize
patches.

## Example

- [backup/kustomization.yml](./.github/testpv/backup/kustomization.yml): create one for each backed up PV (will also
  prune as needed and check integrity).
- To restore a backup, you need to specify a snapshot, review the [end to end test](./.github/workflows/e2e.yml).

