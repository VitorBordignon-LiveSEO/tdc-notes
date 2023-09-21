# Desafios a comunicação e integração de dos entre microsserviços.

## Comunicação Síncrona

### Soap

- Mais comuns para comunicação com sistemas legados ou governamentais

- SUporte integrado de protocolo de segurança

- Pode utilizar de protocolos como HTTP, SMTP, FTP

- Contratos formais e bem definidos WSDL.

- Necessária cautela para tramitação de grande volume de dados.

- Configuração e Implementação podem ser complexos.

### Rest

- Tudo é síncrono, uma abstração de entidades e ou informações.

- Verbos HTTP

- Tanto requisições quanto respostas são multi representacionais, inclusive podem possuir representações diferentes (req em json e res em html).

- Facilidade de identificar erros de resposta através de status HTTP.

### Protocolo HTTP 2.0

- Ao contrário do 1.0 essa versão permite a abertura e mantimento de uma conexão que pode ser usada para trafegar dados do servidor para o endpoint.

### gRPC

- Modelo representacional se baseia na interface definition language (idl) em binários protocol buffers (protobuf)

- Facilidade em identificar erros através de status de resposta

- Contratos formais e definidos através do arquivo IDL.

- Suporte a chamada assíncronas e abertura de canais/sockets entre clientes s servidores

- Suporte para segurança e autenticação TSL/SSL.

### Casos de uso

- Recebimento de dados paginados melhorando performance e evitando ultrapassar limite de memoria do container

- Processamento paralelizado através do canal aberto no protocolo HTTP/2.0

## Comunicação Assíncrona

Como apresentado pela palestrante, o caso de usos deles utilizam -> RabbitMQ, Kafka, Amazon SQS

- Amazon SQS -> Uma boa escolha para projetos pequenos que não consumirão um volume grande de dados trafegados.

- RabbitMQ -> Uma boa forma de implementar o seu próprio messenger broker.

- Kafka -> O mais robusto dos mensageiros, pode causar dores de cabeça devido a dificuldade de implementação, manutenção e monitoramento

## Monitoramento: Service Mesh e Service Discovery

- Service Mesh -> Fornece o maior nível de observabilidade, é uma camada de infraestrutura dedicada a monitorar e administrar comunicação entres serviçps dentro de uma arquitetura de microsserviços.

- Service Discovery -> É o processo de automaticamente identificar serviços ou recursos presentes em uma rede ou sistema distribuído.
