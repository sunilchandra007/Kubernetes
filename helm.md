# Helm Cheatsheet

Helm is a package manager for Kubernetes that simplifies deploying and managing applications using *charts*.

---

## Core Concepts
- **Chart**: A package of pre-configured Kubernetes resources.
- **Release**: An instance of a chart deployed/running in a Kubernetes cluster.
- **Repository**: A collection of charts or storage location for charts.
- **Values**: Default configuration settings for a chart, defined in `values.yaml`.

---

## Repository Management ( local machine )
| Command                     | Description                              |
|-----------------------------|------------------------------------------|
| `helm repo add <repo-name> <repo-url>`| Add a new chart repository              |
| `helm repo list`            | List all configured repositories        |
| `helm repo update`          | Update local cache of repository charts |
| `helm repo remove <repo-name>`   | Remove a repository                     |
| `helm search repo <keyword>` |	Search added repositories for a keyword in charts |
| `helm search hub <keyword>` |  Search for charts in the Artifact Hub or your own hub instance |

**Example**:  
```bash
helm repo add bitnami https://charts.bitnami.com/bitnami

# View a list of all installed plugins
helm plugin list       
```


## Managing Releases ( in k8s namespace / cluster )
| Command	| Description |
|-----------------------------|------------------------------------------|
| helm list | List all deployed releases in the current namespace |
| helm list --all| List all releases, including deleted in the current namespace |
| helm status <release> |	Check the status of a release | 
| helm uninstall <release>	 | Remove a release from the cluster | 
| helm get values <release>	| Retrieve values used for a release |

**Example**:  
```bash
# List all deployed releases
helm list
helm repo update
```
