Cassiano e Charles

Crie um contêiner Docker que contenha uma aplicação web usando Docker Compose para exibir o número de vezes que o servidor foi visitado.

Primeiro, crie o arquivo index.js, o arquivo JavaScript para:

Exibir a mensagem "Número de visitas" no navegador web
Especificar a porta a ser escutada (8080)
Especificar o cliente
Aumentar o número de visitas a cada solicitação ao servidor
E o arquivo package.json para especificar as dependências e os scripts.

Em seguida, construa a imagem node-app a partir do Dockerfile. Comando: docker build -t adarsha/node-app .

E execute o servidor Redis diretamente. Comando: docker run redis

Agora, para configurar a ligação entre dois contêineres, node-app e redis, use o Docker Compose. Crie o arquivo docker-compose.yml e declare a versão a ser usada, os serviços utilizados, como construir a imagem e especifique a porta na máquina local e no contêiner também.

Use o seguinte comando para iniciar o arquivo docker-compose, que configura tudo. Comando: docker-compose up

*Para reconstruir as imagens listadas dentro do docker-compose Comando: docker-compose up --build

*Para fechar vários contêineres do docker-compose Comando: docker-compose down