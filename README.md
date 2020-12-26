# ckad
### switch context
```
kubectl config use-context <context-name> <namespace>
```
```
kubectl config use-context --current --namespace=namepsace_name
```

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
### dns
```
mysql.connect("db-service.dev.svc.cluster.local")
db-service = service name
dev = namespace
svc = service
cluster.local = domain
```
### get namespace
```
kubectl get pods -n argo-cd
```
### create resource in namespace
```
kubectl apply -f pod.yaml -n argo-cd
```
### change namespace in context
```
kubectl config set-context --current --namespace=dev
```
### kubectl imperative commands
#### pods
```
kubectl run nginx-pod --image=nginx:alpine
```
```
kubectl run redis --image=redis:alpine --labels="tier=db"
```
```
kubectl expose pod redis --port=6379 --name redis-service
```
```
kubectl run custom-nginx --image=nginx --port=8080
```
```
kubectl expose pod httpd --port=80 --name=httpd
```
#### config map
```
kubectl create configmap --from-literal=APP_COLOR=blue --from-literal=APP_MOD=prod
```
#### deployments
```
kubectl create deployment redis-deploy -n dev-ns --image=redis --replicas=2
```
```
kubectl create deployment webapp --image=kodekloud/webapp-color --replicas=3
```
