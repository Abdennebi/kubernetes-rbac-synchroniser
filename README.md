# kubernetes-rbac-synchroniser
[![Docker Repository on Quay](https://quay.io/repository/yacut/kubernetes-rbac-synchroniser/status "Docker Repository on Quay")](https://quay.io/repository/yacut/kubernetes-rbac-synchroniser)
[![Docker Pulls](https://img.shields.io/docker/pulls/yacut/kubernetes-rbac-synchroniser.svg?maxAge=604800)](https://hub.docker.com/r/yacut/kubernetes-rbac-synchroniser)
[![Go Report Card](https://goreportcard.com/badge/github.com/yacut/kubernetes-rbac-synchroniser)](https://goreportcard.com/report/github.com/yacut/kubernetes-rbac-synchroniser)


## Requirements

- The service account's private key file: **-config-file-path** flag
- The email of the user with permissions to access the Admin APIs:  **-config-subject** flag

> see guide: https://developers.google.com/admin-sdk/directory/v1/guides/delegation

- The Google Group list per Kubernetes namespace comma separated: **-group-list** flag
- Configure Minimal GKE IAM permissions for each Google Group

> see: https://stackoverflow.com/questions/45945074/iam-and-rbac-conflicts-on-google-cloud-container-engine-gke/45945239#45945239

### Prometheus metrics

- **rbac_synchroniser_success**: Cumulative number of role update operations.
- **rbac_synchroniser_errors**: Cumulative number of errors during role update operations.

### Links

- https://developers.google.com/admin-sdk/directory/v1/guides/delegation
- https://developers.google.com/admin-sdk/directory/v1/guides/manage-group-members
- https://github.com/kubernetes/client-go
- https://github.com/prometheus/client_golang
