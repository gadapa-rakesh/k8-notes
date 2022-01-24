
# K8 Commands

Notes on K8 commands

## Labels  
Get all objects where label env is prod. ignore headers  
` $ k get all --selector env=prod --no-headers `

Selecting a pod by matching multiple labels.  
` $ k get pod --selector env=prod,bu=finance,tier=frontend` 

