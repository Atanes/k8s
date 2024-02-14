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

Visualizar recursos utilizados pelo pod:  
kubectl top pod nome-pode

Rodar um pod de forma iterativa (-it) com o nome de <fortio> usando a imagem <fortio/fortio> e apagar (--rm) quando o processo for finalizado:  
Obs.: **-- load -qps 800 -t 120s -c 70 "http://goserver-service/healthz"** são comandos do fortio  
kubectl run -it --image=fortio/fortio fortio --rm  -- load -qps 800 -t 120s -c 70 "http://goserver-service/healthz"  

Acompanhar a execução de um comando na janela do prompt:  
watch -n1 kubectl get hpa

