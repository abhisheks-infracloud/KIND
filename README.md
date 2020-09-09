## Quickly provision a K8s cluster using [KIND](https://kind.sigs.k8s.io/)

### Install KIND 
https://kind.sigs.k8s.io/docs/user/quick-start/#installation

### Create K8s cluster
If you want to create a single node K8s cluster quickly, just run the command

```bash
$ kind create cluster
```
By default, the cluster will be given the name kind. Use the --name flag to assign the cluster a different context name.
If you want the create cluster command to block until the control plane reaches a ready status, you can use the --wait flag and specify a timeout. To use --wait you must specify the units of the time to wait. For example, to wait for 30 seconds, do --wait 30s, for 5 minutes do --wait 5m, etc.

Create K8s cluster using KIND configuration file
For a sample kind configuration file see [kind-example-config](https://raw.githubusercontent.com/kubernetes-sigs/kind/master/site/content/docs/user/kind-example-config.yaml). To specify a configuration file when creating a cluster, use the --config flag:

```bash
kind create cluster --config kind-example-config.yaml
```
