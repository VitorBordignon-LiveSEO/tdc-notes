# Custo do JS para sua aplicação Web

## Vamos entender o problema

Em media sites mobile carregam em 10 segundos. 53% dos usuários abandonam o site se não carregar em 3 segundos.

Sites interativos em menos e 5 segundos tem

- 70% de permanecia em seu site

- Mais visibilidades em ADS

- 200kb de JPG e JS não significam a mesma coisa. Para atingir 5 segundos de interação, 300kb de JS seria o máximo aceitável.

É necessário tem em mente como a sua aplicação funciona na maior variedade de dispositivos, visto que seus consumidores podem ter uma vasta gama de dispositivos.

Existe dados para mostrar que cada vez enviamos mais JS ao cliente e mais ainda JS que não será executado

## Como podemos medir o problema

Devemos estar atentos as métricas do Core Web Vitals

- **LCP** -> 75% de visibilidade do resultado final da página, segmentado através de dispositivos móveis e desktop

- **FID** -> Tempo de respostas as primeira interações do usuário com elemento visíveis da sua página.

- **CLS** -> Impacto da instabilidade visual da sua página durante o carregamento ao mudar os elementos de tamanho e lugar

**Evolução do Core Web Vitals** -> Essas métricas estão em evolução e novas métricas podem ser adicionadas ao Core Web Vitals ou outras podem ser removidas.

Podemos instalar o lighthouse em nosso terminal e podemos integrar ela com nossas actions para que possamos automaticamente travar atualizações que danifiquem as nossas métricas de performance.

Performance não deveria ser algo que somente é pensado em situações de emergência. O próprio google usa essas métricas para priorizar seus resultados de buscas.

Podemos usar ferramentas para analisar o bundle da nossa página com ferramentas como Webpack analyzer

Devemos ter em mente o tamanho das dependências que usamos

Podemos usar code-splitting bundles par minimizar o tamanho da nossa aplicação na qual podemos fazer lady loading do nossos componentes conforme eles forem requiridos

Podemos fazer lazy loading por rotas também.

Dynamic imports são uma ótima ferramenta para minimizar a quantidade de JS que utilizamos, pois somente importamos os componentes quando são requisitados.

## Server side rendering

Método pelo qual carregamos tudo no servidor e enviamos tudo pronto para o cliente consumir. Melhora a indexação e o ranking da sua página no Google.

O SSR gera um maior custo de infraestrutura para sua aplicação, aumento da complexidade de deploy e amento de pontos de falha.

Tenha certeza que sua página esta sendo reidratada corretamente.

## Melhores Práticas atuais e o que o futuro nos aguarda

- E se o carregamento e reidratação for processivo/seletivo. Precisamos hidratar em uma vez só, ou seria melhor hidratar aonde o houve mudança na página.

- **Island Architecture** -> Divide naturalmente a plicação em areas menores que podem ser carregadas individualmente.

- **React Server Components** -> Traz a estratégia de SSR nativamente para o ecossistema React mas tem como contraponto a necessidade de maior foco na infraestrutura da aplicação.
