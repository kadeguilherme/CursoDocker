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
