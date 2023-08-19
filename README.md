# assessment-graphql-guide


O objetivo sera desenvolver uma api graphql utilizando nestjs, que permita realizar operacoes em entidades chamadas "cubos". A unica operacao necessaria sera "calcular volume" para cubos que foram cadastrados previamente. Segue abaixo uma lista mais especifica dos requisitos:


## schema 

O tipo "Cubo" deve ser a seguinte schema na api graphql: 


```graphql

  type Cubo {
     altura: Float!
     largura: Float!
     comprimento: Float!
  }

```

## Mutations 

1 - A API graphql deve oferecer uma *mutation* para cadastrar novos cubos, os inputs para essa mutation devem ser "altura", largura, e comprimento, sendo assim a mutation devera ter esse formato: 

```graphql
  cadastrarCubo(altura:Float!, largura: Float, comprimento: Float!): Cubo!
```

Deve haver uma camada de persistencia para os cubos cadastrados, usando o banco de dados de sua preferencia.

## Queries

2 - A API graphql deve oferecer uma *query* para calcular o volume de cubos cadastrados previamente :

```graphql
  volume(cuboId:Integer!): Float!
```

3 - A API graphql deve oferecer uma *query* para retornar os dados de um cubo cadastrados previamente:

```graphql
  cubo(cuboId:Integer!): Cubo!
```

## Testes

4 - Deve haver um teste unitario ( pode user utilizando jest ou outro framework de test para node ) que garata que a funcao de calcular volume esta correta.

## Execucao 

5 - a applicacao deve ser iniciada atraves do commando `yarn start` ou `npm start`

### Observacoes

A applicacao deve ser enviada para o repositorio publico do github, ou outro repositorio de sua preferencia

### Resources : 

https://docs.nestjs.com/graphql/quick-start
