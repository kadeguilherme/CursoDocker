# Minikube
  Com o Minikube criamos uma implementação leve do Kubernetes que cria uma VM em sua maquina local e implanta um cluster simples contendo apenas um nó.
 
## Iniciando o Minikube
  minikube start --driver=docker
  
  DRIVER
  - virtualbox
  - hyperv
  - docker 
 
 > **Observação:** Sempre que o computador for reiniciado deveremos iniciar o Minikube

## Acessando dashboard do Kubernetes 
  
Comandos para acessar dashboard:
```
$ minikube dashboard
```
ou 
```
$ minikube dashboard --url
Obter apenas a URL
```
## Checando Pods
Veriticar os Pods:
```
kubectl get pods
```

Verificar os Pods com mais detalhes 
```
kubectl describe pods
```

## Criando Service
```
kubectl expose deployment <NOME> --type<TIPO> --port=<PORT>
```
NOME = Nome criado do Deployment
TIPO = Existem varios tipos de serviços, porem LoadBalancer é o mais comum
PORT = A porta para o servico ser consumindo

## Gerando IP de acesso
```
minikube service <NOME>
```
