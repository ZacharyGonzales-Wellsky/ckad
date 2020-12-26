# ckad
### context
```
kubectl config use-context <context-name> <namespace>
```
```
kubectl config use-context --current --namespace=namepsace_name
```
```
kubectl config set-context --current --namespace=dev
```

### dns
```
mysql.connect("db-service.dev.svc.cluster.local")
db-service = service name
dev = namespace
svc = service
cluster.local = domain
```
### namespace
```
kubectl apply -f pod.yaml -n argo-cd
```
```
kubectl get pods -n argo-cd
```

### pods
```
kubectl apply -f <pod-file>
```
```
kubectl apply -f <pod-file>
```
```
kubectl get pod <pod-name> -o yaml > pod.yaml
```
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
### config map
```
kubectl create configmap --from-literal=APP_COLOR=blue --from-literal=APP_MOD=prod
```
```
kubectl create configmap --from-file=<path-to-file>
```
```
kubectl create configmap --from-file=<path-to-file>
```
```
kubectl create configmap --from-file=app_config.properties
```
### replicasets
```
kubectl create -f replicaset-definition.yml
```
```
kubectl get replicaset
```
```
kubectl delete replicaset myapp-replicaset
```
```
kubectl replace -f replicaset-def
```
```
kubectl scale replicaset --replicas=6 new-replica-set
```

### deployments
```
kubectl create deployment redis-deploy -n dev-ns --image=redis --replicas=2
```
```
kubectl create deployment webapp --image=kodekloud/webapp-color --replicas=3
```
```
kubectl get deployments
```
```
kubectl create deployment --image:httpd:2.4-alpine
```
```
kubectl scale deployment --replicas=3 httpd-frontend
```
