# alura-docker
Projeto do curso de Docker

Para o projeto funcionar é necessário baixar as seguintes imagens no docker-hub

docker pull douglasq/alura-books:cap05
docker pull mongo

# Criando a Rede
- docker network create --driver bridge minha-rede

Existe um arquivo serve.js que carrega algumas dependencias


# Subindo a imagem  MONGO na rede criada (minha-rede)

- docker run -d --name meu-mongo --network minha-rede mongo

# Subindo a imagem do servidor node js na mesma rede criada (minha-rede)

- docker run --network minha-rede -d -p 8080:3000 douglasq/alura-books:cap05


Existe duas rotas locais(localhost) na porta 8080

"/"- Exibe os dados dos livros em uma interface que estão no banco MONGO

"/seed" preeenche os dados dos livros no mongoDB