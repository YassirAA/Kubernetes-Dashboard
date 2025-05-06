# Kubernetes-Dashboard

## Muntar Dashbaord
```bash
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml
```

## Com ho fem servir

Revisem que els pods estan be 
```bash
kubectl get pods -n kubernetes-dashboard
```

## Despres ens aixequem la porta d'entrada
```bash
kubectl -n kubernetes-dashboard port-forward svc/kubernetes-dashboard-kong-proxy 8443:443
```
## Una vegada fet aixo puc anar el meu ordinador portatil i crear un tunel ssh
```bash
ssh -L 8443:localhost:8443 retroreel@192.168.0.100
```
## I anem al navegador i posem 
```bash
https://localhost:8443/
```
