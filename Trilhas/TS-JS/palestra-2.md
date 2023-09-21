# Construindo seu próprio Google Meet ou Teams

## O que é WebRTC

Tecnologia nativa de browsers que permitem uma comunicação direta entre suários através de browser através dela é possível compartilhar áudio, video e demais dados

Surge em 2009 por iniciativa do google

Para estabelecer comunicação é necessário um servidor para intermediar esse primeiro contato, operação conhecida como Signaling

- Signaling é o momento onde o usuário candidato da conexão envia uma oferta(offer SDP) com um pacote de dados para outro usuário, que aceitado irá enviar de volta uma Resposta (answer SDP) e a partir dai a comunicação pode iniciar entre os dois.

- Peer2Peer -> A conexão se torna mais rápida e eficiente se comparado as outras tenologias de stream, sendo necessário um servido externo apenas para realizar o primeiro contato.

- Turn Server -> Porem caso a comunicação entre essas duas pontas caia, uma estrategia chamada de relay server pode ser usada para manter a conexão.

- Cenário de falha -> Servidor que irá assumir o controle a comunicação entre os peers, sempre em cenários de falha.

## Casos de Uso

O WebRTC se tornou tão popular dado sua tecnologia, qe grande players do mercado estão usando em alguma parte do seus principais sistemas.

- Google -> Meet, Hangouts

- WebWhatsApp -> Video Calls

- Facebook -> Messenger

- Discord

## WebRTC API's

Essa API já esta nativamente implementada em browsers

RTCPeerCOnnection -> Principal responsável por criar o pacote de oferta SDP e armazena-los quando a oferta recebida de outro peer. TOdo ciclo de vida de uma comunicação peer2peer é feira por ele

RTCDataChannel -> Canal entre dois pares sobre os quais você pode enviar e receber dados. Vai funcionar como um túnel que conecta os dois peers diretamente para transferência e dados.

## Arquitetura

O Signaling Server não esta ligado diretamente a tecnologia é um facilitador que dá suporte a transferência de dados para estabelecer uma conexão direte entre os usuários.

**SDP** (Session Description Protocol)

- Dados em chave-valor necessários para a oferta/resposta da conexão

- Configuração de mídia, formato, resolução e default constraints

- Protocol de transferências, largura de banda

**STUN** (Session Transversal Utilities for NAT)

- É o componente que tem por responsabilidade descobrir o ip publico eo mapeamento de portas de um , que geralmente está atrás de um NAT ou firewall.

**ICE Candidate**

A sigla ICE significa Interactive COnnectivity Establishment e os ICE candidates são informações sobre possíveis maneiras de estabelecer uma conexão direta entre os dispositivos, superando os desafios de rede NAT e firewalls,

**Turn server**

O turn server cuja sigla significa Transversal using relay around NAT é um componente crucial no contexto do WebRTC que desempenha um papel fundamental na resolução de desafios de conectividade.

## Aplicação

- WebRTC puro

- Criação de uma sala

- Preparação da conexão entre ambos

- Inicialização da conexão.
