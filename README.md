# PFA :: Docker :: Desafio 02
## Subindo serviços
```
docker compose up -d
```
ou
```
docker-compose up -d
```
## Acessando o serviço
[http://localhost:8000](http://localhost:8000)

p.s.: verificar disponibilidade da porta no host

Resposta esperada:

```javascript
{
   "modules":[
      {
         "id":7,
         "module":"Arquitetura e Projeto Pratico - Codeflix"
      },
      {
         "id":5,
         "module":"Autenticacao e Keycloak"
      },
      {
         "id":3,
         "module":"Comunicacao"
      },
      {
         "id":1,
         "module":"Docker"
      },
      {
         "id":6,
         "module":"Domain Drive Design e Arquitetura Hexagonal"
      },
      {
         "id":2,
         "module":"Fundamentos de Arquitetura de Software"
      },
      {
         "id":4,
         "module":"RabbitMQ"
      }
   ]
}

```
## Dockerize
- ao subir o serviço da api, aguarda disponibilidade do banco mysql checando resposta da chamada tcp na porta 3306 do serviço do banco
- ao subir o nginx, aguarda resposta 200 da chamada http ao serviço da api