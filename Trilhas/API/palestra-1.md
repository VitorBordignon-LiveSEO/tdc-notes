# Palestra 1 - Construindo APIS resilientes

- O que é versionamento - Uma forma de diferenciar pontos no temo em que a api muda de uma fora que exige que os con su m idores da api modifiquem o seu aplicativo.

- Dar a possibilidade de que o consumidor da api possa transitar entre as versões, mantendo compatibilidade entre as versões

- **Major** -> QUando impacta em braking changes

- **Minor** -> pode ser ignorado por clientes que não querem suar esses novos recursos.

- **Patch** -> são pequenas mudanças que não afetam o código.

- Uma Api resiliente é uma API que consegue se comportar de forma efetiva em condições adversas ( trafego excessivo, lentidão de rede )

- O versionamento pode ser uma característica fundamental para a resiliência de uma API

- O versionamento pode ser feio através do path da api (https://apiexample/api/v1/categories)

- O versionamento pode ser feito por meio de query params (https://apiexample/api/categories?v=1.1)

**Prós** -> Fácil de implementar e usar. Pod definir versão mais recene como padrão.

- O versionamento pode ser feito por meio de custom headers (https://apiexample/api/categories, curl -h "accepts-version:v1")

**Prós** -> Não adiciona preenchimento na URI subversões podem ser adicionadas como cabeçalhos

- O versionamento pode ser feito por meio de content negotiation (GET : https://apiexample/api/categories, Accept: application/vnd.example.api+json;version=2)

## Documentação da API

Benefícios da documentação e versionamento

- **Clareza e compreensão** -> Permite maior compreensão e compartilhamento das funcionalidades e possibilidades da API, tal como guias de migração.

- **Mudanças controladas** -> Permite maior controle sobre as mudanças aplicadas na api

- **Compatibilidade** -> Mantendo a compatibilidade entre demais versões da aplicação

- **Aviso de descontinuação** -> Manter os consumidores da API informados do cronograma de depreciação para dita API. Evitar ao máximo descontinuações abruptas.

## Melhores praticas de documentação

- **Estrutura de documentação por versão** -> Organize a sua documentação de forma que cada versão da PAI tenha sua seção separada

- **Destaque as diferenças** -> Forneça uma seção destacada que descreva as principais diferenças entre as versões

- **Exemplos de migração** -> Forneça exemplos de como se adaptar a versões mais recentes da API

- **Indicadores de obsolência** -> Indicar aos consumidores quando uma versão de uma API ira deixar de ter suporte.

## Ferramentas

- Swagger

- Postman

- Insomnia

- Readme

## Pontos de atenção

- Use uma convenção de nomenclatura clara e não escolha números arbitrariamente.

- Defina um cronograma para versões obsoletas ou permita Apis side by side.

- Tenha uma documentação clara e detalhada estabelecendo suas diretrizes de controle de versão.

- Faça adições compatíveis com versões anteriores.

- Automatize a segurança das suas API -> Você pode fiar tranquilo sabendo que sua API está protegida com automação.
