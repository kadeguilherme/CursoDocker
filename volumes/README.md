# Docker Volumes
A principal função do volume é persistentir os Dados. Sem os volumes apos criamos um container com algum imagem e remove o container, perderemos todos os aqruivos.

  # Tipos de volumes
   - Anonymous : Diretorios criados pela **flag -v** porém com um nome aleatorio.
   - Named : São volumes com nomes, podemos nos referir a estes facilmente e saber para que são utilizados no nosso ambiente.
   - Bind Mounts : Uma forma de salvar dados na nossa maquina, sem o gerencimento do Docker, informamos um diretório para este fim.
