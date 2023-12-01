# Cluster API Provider Linode
A [Cluster API](https://cluster-api.sigs.k8s.io/) implementation for the [Linode](https://www.linode.com/) to create kubernetes clusters.

### Local development with Tilt

For local development execute the following `make` target:

```bash
make tilt-cluster
```

This command creates a Kind cluster, and deploys resources via Tilt. You can freely change the code and wait for Tilt to update provider.

### Local debugging with Mirrord

You can run your local version of the provider on any remote cluster via [Mirrord](https://github.com/metalbear-co/mirrord):

```bash
make mirrord
mirrord exec go run ./cmd/main.go -f .mirrord/mirrord.json
```

For local debugging, please install Mirrord plugin into your favorite IDE.
