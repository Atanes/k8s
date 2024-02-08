# k8s -> FullCycle Kubernets

## Comandos

Para "entrar" no POD:  
kubectl exec -it pod-name -- bash

Para ver os logs do POD:  
kubectl logs pod-name

Fazer redirecionamento de portas:  
kubectl port-forward svc/goserver-service 8080:80

Visualizar os Pods:  
kubectl get pods

Visualizar os deployments:  
kubectl get deployments

Visualizar os configmap:  
kubectl get configmaps

Visualizar os services:  
kubectl get svc

Aplicar configurações:  
kubectl apply -f nome-arquivo.yaml (service.yaml, deployment.yaml, configmap.yaml, etc.)
