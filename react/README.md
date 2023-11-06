# funcionamento do docker-compose:

- No Dockerfile criamos uma imagem baseada no node.js
- Dentro da imagem inserimos um codigo fonte que está neste repositorio
  - RUN git clone https://github.com/ClauHenrique/homepage-docker.git

- O docker-compose levantará uma imagem a partir deste Dockerfile. Então sertifique-se de que os arquivos Dockerfile e docker-compose.yml estejam no mesmo diretório.
- No parâmetro "command", definimos alguns comandos a serem executados quando o container for levantado
  - cd ./homepage-docker: irá entrar dentro da pasta do projeto que foi clonado do github
  - git pull: pega a última atualização do repositório
  - npm i: instala dependências
  - npm start: executa o react

## executando o container:
- baixe os arquivos Dockerfile e docker-compose.yml que estão dentro deste diretório "react"
- dentro do diretório execute docker-compose up
