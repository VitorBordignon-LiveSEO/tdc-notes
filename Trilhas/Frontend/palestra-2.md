## Arquitetura Front-End

## Prazo Escopo e Pessoas

A maior dificuldade de uma arquitetura não é a escolha da mesma. Mas sim, garantir a adesão da equipe ao processo e a arquitetura escolhida em meio a troca de membros de equipe e mudanças de escopo

## Princípios de Design de Classe Orientado a Objtos

- Aberto-Fechado.

- Substituição de Liskov.

- Inversão de dependência.

- Interfaces devem ser separadas para que classes dependam somente dos métodos que implementam.

- Responsabilidade única.

## Técnicas e soluções

- **Arquitetura limpa** -> Padronizar e organizar o código para facilitar o reuso independente de bibliotecas

**Camadas** -> As diferentes areas de um software deve estar em lugares diferentes.

- _Entidades_ -> Regras de negócio

- _Casos de uso_ -> Regras da aplicação

- _Apresentadores_ -> Acesso a dados

- _UI_ -> Interface do usuários

As camadas favorecem a escrita de testes, interdependência de UI, interdependência de DB

## Monorepo !== Monolito

- SImplifica o compartilhamento de código

- Facilita refatorações entre projetos

- Reduz o custo na criação de novas bibliotecas, micro serviços e microfrontends.

Chamamos de monorepo se projetos dependem uns dos outros, para que possam compartilhar código. Em alterações, não buildamos nem testamos todos os projetos, apenas executamos novamente projetos que podem ser afeados pela alteração em questão.

## Polirepos vs Monorepos

**Cada no repo no polirepos significa**:

- COnfigurar as ferramentas

- Configurar ambientes de CI

- Adicionar commiters

- Configurar a publicação

**Com monorepo significa**:

- Reuso de implementações

- Mesma configuração de CI

- Não precisa publicar pacotes

- Maior controle de qualidade.
