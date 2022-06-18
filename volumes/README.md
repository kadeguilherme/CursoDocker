# Docker Volumes
A principal função do volume é persistentir os Dados. Sem os volumes apos criamos um container com algum imagem e remove o container, perderemos todos os aqruivos.

  # Tipos de volumes
   - Anonymous : Diretorios criados pela **flag -v** porém com um nome aleatorio.
   - Named : São volumes com nomes, podemos nos referir a estes facilmente e saber para que são utilizados no nosso ambiente.
   - Bind Mounts : Uma forma de salvar dados na nossa maquina, sem o gerencimento do Docker, informamos um diretório para este fim.

## Para ver os volumes usamos:
 ```
  docker volumes ls
  Podemos ver todos os volumes do ambiente
```

  ## Volume Anonymous
  
  Para você ter o nubank clone no seu celular digite o seguinte comando no seu terminal
  
  Criando Volume Anonymous
  ```
  docker run -v /data
```
  Onde **/Data** será o diretorio que contém o volume anonimo
  
  ## Volume Named
   Criando Volume Named
  ```
  docker run -v nomedovolume:/data
```

  ## Volume Bind Mounts
   Criando Volume Bind Mounts
  ```
  docker run -v /dir/data:/data
```

  ## Criando um Volume 
   Podemos criar criar um volume manualmente 
  ```
  docker volume create <none>
```
