

# K8 Notes

Notes on K8 commands
> **Note:** Please note that k is an alias for kubectl <br/> `$ alias k=kubectl`

## Labels  


## Updates and Rollbacks
|Commands|Comments|
|--|--|
|`k create -f <deployment-file>`|Create a deployment|
|`k get deployments`|Use get to get the current deployments|
| ` k rollout status <deployment>` | Status of the rollout |
| `k rollout history <deployment>` | history and revision of the rollout  |
| `k describe deployment <deployment>` | Find deployments in detail   |
| `k apply -f <deployment-filename>` <br/> `k set image <deployment-name> <image-name>=<image-version>` | Update the deployment |
|`k rollout undo <deployment-name>`  | Rollback deployment  |

**Deployment Strategies:**

 1. **Re-create strategy:** delete everything and bring up everything. Not a default. There will be down time
 2. **Rolling update:** Take down the older and bring up the newer version. default strategy if one not given while creating deployments

> **Note:** a new replica set is created when rolling update strategy is followed
