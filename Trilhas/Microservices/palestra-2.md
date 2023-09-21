# tRPC - quando usar, vantagens e desvantagens.

## Ficado na mesma página: modelo cliente/servidor

A arquitetura mais padronizada, na qual o cliente requer algum serviço que será fornecido pelo servidor.

O contrato entre entre servidor entre cliente e entre serviços determinado por interfaces quer regulam a entrada e saida de dados, tal como os requisitos de autenticação

## Schema-driven development

Schemas vao te obrigar a respeitar o contrato de comunicação.

## tRPC

- Uma nova forma de criar APIs. Ele é totalmente Typesafe, ou seja, os contratos serão respeitados para o estabelecimento da comunicação, sem a criação de Schemas.

- Sem geração automática de código.

- Como o tRPC é typescript based, ele vai usar essas regras de validação da linguagem para validar os contratos de comunicação

- O tRPC foi definido na RFC 1050 no final dos anos 1980.

- RPC == Remote Procedure Call

- No Rpc o cliente faz chamada de função remota a um servidor. Já no rest o cliente solicita ao servidor que executa uma ação a um recurso. Ações limitadas ao CRUD transmitidas como verbos http

- O rest pode transmit qualquer formato de dados na mesma api (JSON, XML)

- No Rpc o formado de dados é selecionado pelo servidor. O cliente não tem flexibilidade.

- No RPC, você chama uma function e obtém uma resposta. No REST você chama um endereço URL e ontem uma resposta. O tRPC combina conceitos do Rest e do GraphQL

- Com o tRpc vc vai comunicar seu backend e seu frontend garantindo type safety.

- Suporta apenas TypeScript

- Ainda é dependente de um monorepo.

- Considere usar essa tecnologia com BFF's

## gRPC != tRPC

- gRPC usa protobufs e o schema é definido em um arquivo .proto.

## Termos comuns no RPC

- Procedure

- Query

- Mutation

- Subscription

- Router

- Context

- Middleware

- Validation

## Exemplos práticos

## Conclusão

## Próximos passos
