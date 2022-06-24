# Docker Network
Uma forma de gerenciar conexeão do Docker com outras plataformas ou até entre containers

  # Tipos de Drives (Rede)
   - Bridge : Default. Utilizado quando containers precisam se conectar
   - host : Permite a conexao entre um container a maquia que está hosteando o Docker
   - Macvlan : Permite conexao a um container por um MAC address
   - none : Remove todas conexões de rede de um container
   - Plugins : Permite extensões de terceiros para criar outras redes

## Listando Network usamos:
 ```
  docker network ls
  Podemos ver todos os networks do ambiente
```

  ## Conectando Container
  ```
  docker network <rede> <container>
```

  ## Desconectando Container
  ```
  docker network disconnnect <rede> <container>
```

  ## Inspecionando Redes
  ```
  docker inspect <nome>
```
  
  ## Criando Network
  ```
  docker network create <nome>
```
  
  ## Removendo Network
  ```
  docker network rm <nome>
```

  ## Especifica o tipo de rede e o Host docker internal
  ```
  docker run -d --network=host --add-host host.docker.internal:127.0.0.1  -p 5000:5000 --name flaskhostcontainer --rm flaskhos
```
