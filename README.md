# ckad
### create pod
```
kubectl apply -f <pod-file>
```
### edit pods
```
kubectl get pod <pod-name> -o yaml > pod.yaml
```
```
kubectl edit pod <pod-name>
```
### create replicaset
```
kubectl create -f replicaset-definition.yml
```
### get replicaset
```
kubectl get replicaset
```
### delete replicaset
```
kubectl delete replicaset myapp-replicaset
```
### replace replicaset
```
kubectl replace -f replicaset-def
```
### scale replicaset
```
kubectl scale replicaset --replicas=6 new-replica-set
```
### get deployments
```
kubectl get deployments
```
### create a deployment using flags
```
kubectl create deployment --image:httpd:2.4-alpine
```
### scale deployment
```
kubectl scale deployment --replicas=3 httpd-frontend
```
