# Microservices, Mensageria e Escalabilidade com Kubernetes + KEDA

## Aplicações modernas: alguns aspectos importantes

- Alta disponibilidade

- Escalabilidade horizontal

- Comunicação assíncrona, Mensageria, Eventos

- Containers

- Microsserviços

## Mensageria e aplicações

- Facilidade de integração

- Desacoplamento

- Tolerância a falhas

- Escalabilidade.

## Como o Kubernetes pode ser útil

- Orquestração de containers

- Autoscaling de aplicações

- Mecanismos de Health Check

## Horizontal pod autoscaling

- Mecanismo nativo do Kubernetes para escalabilidade horizontal

- Baseado em métricas omo uso de CPU, média de utilização de memória

- Limitações com métricas customizadas.

## Métricas customizadas X escalabilidade

- Eventos acumulados para processamento

- QUantidade de mensagens enfileiradas para processamento

- Requisições HTTP po segundo

- Registros a processar em um banco de dados

## Como escalar com base em métrica customizadas

- O projeto KEDA (Kubernetes Event-driven autoscaling) pode ser uma excelente resposta! site oficial: https://keda.sh

- Escalabilidade horizontal de aplicações de fo rma descomplicada

- Uso da HPA no Kubernetes

- Um projeto open source apoiado pela Cloud Native Computing Foundation

- Facilmente instalável via Helm

- Suporte a dezenas de tecnologias, através de Scalers qe incluem soluções de mensageria/eventos, bancos de dados, monitoramento

- Um scaler se baseia em uma métrica customizada.

- Autoscaling pode ser combinada com tecnologias como o Cron. (Escalar a aplicação em horário comercial e desescalar ela em momento de menos tráfego)

- Objetos estendem um deployment, com as definições contando em um arquivo YAML

- **ScaledObject**: estrutura com as regras Scaler + Trigger para efetuar o autoscaling de uma aplicação

- **Trigger Authentication** -> configura acesso a um recurso.

- Um repositório de teste pode ser encontrado em -> https://github.com/renatogroffe/KEDA-TDCBusiness2023/blob/main/src/BaseContagemKafka.sql

```yml
# Documentacao Apache Kafka: https://keda.sh/docs/2.11/scalers/apache-kafka/
apiVersion: keda.sh/v1alpha1
kind: TriggerAuthentication
metadata:
  name: workercontagem-triggerauth-kafka
spec:
  secretTargetRef:
    - parameter: sasl
      name: workercontagemsecret
      key: SaslApacheKafka
    - parameter: username
      name: workercontagemsecret
      key: UsernameApacheKafka
    - parameter: password
      name: workercontagemsecret
      key: ConnectionApacheKafka
    - parameter: tls
      name: workercontagemsecret
      key: TlsApacheKafka
---
apiVersion: keda.sh/v1alpha1
kind: ScaledObject
metadata:
  name: workercontagem-kafka-scaledobject
spec:
  scaleTargetRef:
    name: workercontagem
  pollingInterval: 45
  minReplicaCount: 2
  maxReplicaCount: 10
  triggers:
    - type: kafka
      metadata:
        bootstrapServers: resource.servicebus.windows.net:9093
        consumerGroup: workercontagem
        topic: topic-contagem
        lagThreshold: "5"
        activationLagThreshold: "1"
        offsetResetPolicy: latest
      authenticationRef:
        name: workercontagem-triggerauth-kafka
```
