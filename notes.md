
# K8 Notes

Notes on K8 commands

## Labels  


## Updates and Rollbacks
Create a deployment   
`k create -f <deployment-file>`  
Use get to get the current deployments  
`k get deployments`  
Status of the rollout  
` k rollout status <deployment>`  
history and revision of the rollout  
`k rollout history <deployment>`  
Find deployments in detail  
`k describe deployment <deployment>`  
Update the deployment   
`k apply -f <deployment-filename>`  
`k set image <deployment-name> <image-name>=<image-version>`  
Rollback deployment  
`k rollout undo <deployment-name>`  

There are 5 deployment strategies

 1. **Re-create strategy:** delete everything and bring up everything. Not a default. There will be down time
 2. **Rolling update:** Take down the older and bring up the newer version. default strategy if one not given while creating deployments

**Note:** a new replica set is created when rolling update strategy is followed
