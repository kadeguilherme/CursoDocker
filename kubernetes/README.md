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

## Verificando serviços

```
kubectl get services
```
```
kubectl describe services/<NOME>
```
## Replicando aplicacao
```
kubectl scale deployment/<NOME> --replicas=<NUMERO>
```

## Atualizacao de imagem
Após subir a nova imagem no Hub 
Usamos o comando para atulizar os pods
```
kubectl set image deployment/<NOME> <NOME_CONTAINER>=<NOVA_IMAGEM>
```

## Fazendo RollBack

Com o seguinte comando verificamos uma alteracao
```
kubectl rollout status deployment/<NOME>
```
Para volta a versão anterior
```
kubectl rollout undo deployment/<NOME>
```

