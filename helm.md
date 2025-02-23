# Helm Cheatsheet

Helm is a package manager for Kubernetes that simplifies deploying and managing applications using *charts*.

---

## Core Concepts
- **Chart**: A package of pre-configured Kubernetes resources.
- **Release**: An instance of a chart deployed to a cluster.
- **Repository**: A storage location for charts.
- **Values**: Customizable settings for a chart.

---

## Repository Management
| Command                     | Description                              |
|-----------------------------|------------------------------------------|
| `helm repo add <repo-name> <repo-url>`| Add a new chart repository              |
| `helm repo list`            | List all configured repositories        |
| `helm repo update`          | Update local cache of repository charts |
| `helm repo remove <repo-name>`   | Remove a repository                     |

**Example**:  
```bash
helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
```


## Managing Releases ( in k8s namespace / cluster )
| Command	| Description |
|-----------------------------|------------------------------------------|
| helm list | List all deployed releases |
| helm list --all| List all releases, including deleted |
| helm status <release> |	Check the status of a release | 
| helm uninstall <release>	 | Remove a release from the cluster | 
| helm get values <release>	| Retrieve values used for a release |

**Example**:  
```bash
# List all deployed releases
helm list
helm repo update
```
