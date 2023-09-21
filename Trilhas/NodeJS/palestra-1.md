# Apify e Crawlee - transformando nodejs na melhor ferramenta de scraping

Uma das dificuldades principais dos WebScrapers é relacionada a escalabilidade

## Introdução

Ambos os termos consistem na ideia de capturar dados de páginas web, porém enquanto o web crawling o spidering consiste em coletar e rastrear dados de páginas web inteira e também páginas que estão associadas a elas por meio de navegação, o webscraping é apenas o conceito de coletar dados específicos de páginas web.

Caso você já tenha se aventurado pelo mundo dos webcrawlers de forma mais profunda, percebeu que eles vão muito além de fazer seletores para o HTML, eles consistem em construir algo que scale a ponto que seja possível coletar os dados de forma independent autossustentável e rápida.

O mundo dos web scraping é muito vasto e com diversa soluções, sendo algumas como, BS$, Selenium, puppeteer, playwright e várias outras. Mas é uma crença popular dizer que o python, é a ferramente superior para trabalhar com crawlers, devido a sua comunidade e ferramentas de analise e visualização de dados, como onumpy, pandas. També por frameworks para spidering já existents como o scarapy.

## Crawlee

O framework de webscraping para mudar o jogo sem sair do contexto do nodejs.

Ele vai adicionar funcionalidades para criação de crawling e spidering escalável em conjunto com as ferramentas já existentes.

- Filas de requisição
- Proxy
- Exception handing
- Fingerprint generation
- Data storing
- Concorrência

Essa ferramenta é um super-set de ferramentas como Puppeteer, Cheerio e Playwright

### Como essa ferramente funciona

**Where** -> onde estou buscando dos, urls, chaves únicas e parâmetros.

**What** -> o que estamos buscando ná paginas e o conjunto e funções para mapear os dados.
