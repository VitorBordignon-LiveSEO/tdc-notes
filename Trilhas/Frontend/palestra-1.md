# Segurança no Front-end

## Cookies e Tokens

**Cookies**

- Armazenados no navegador ou localmente

- Tema período de duração determinável

- São mais vulneráveis a acessos de terceiros não dão segurança aos dados.

**Tokens**

- Strings criptografas com informações de sessão

- Tem período de duração determinável

- São mais seguros para se armazenar informações de autenticação

## SQL injection

Um invasor insere comandosSQL em formulários de entrada ou URL, obtendo assim acesso não autorizado ao banco e dados

Para prevenir a injeção de SQL, os desenvolvedores devem garantir que todas as entradas dos usuários sejam validades e filtradas antes de serem passada para o banco de dados.

Também deve-se limitar privilégios do banco de dados e tratas as consultas.

## Vulnerabilidades de configuração

Um aplicativo é configurado incorretamente, permitindo que invasores tenham acesso não autorizado

Para prevenir vulnerabilidades de configuração OS desenvolvedores deve garantir que todas as on figurações de segurança sejam corretamente valiadas e autenticadas

## Autenticação e autorização

- Manter mensagens de erro genéricas

- Utilizar captcha e MFA

- Níveis de acessos ben gerenciados

- Criptografias e tokens

- Respostas HTTP corretas

- Formulários semânticos.

## Ferramentas e ações aliads

- OWASP Top Open

- Ferramentas de testes de segurança: OWASP ZAP, Nmap, Burp Suite, Nessua

- Instruindo ao usuário a usar senhas fortes

- Controle de tentativas e acesso

- Criptografia

## Leve em conta isso

- Quantidade de dados necessários em formulários.

- LGPD.

- Atrito e exposição

## Em resumo

Utilizar a autenticação para garantir que apenas usuários autorizados tenham acesso à aplicações e uas funcionalidades.

Atualizar regularmente todos os softwares e bibliotecas usadas na ap lição, para corrigir vulnerabilidade conhecidas.

Utilizar criptografia para dads sensíveis, atende-se também aos métodos de armazenamento de dados de sessão do usuário.

Validar todas as do usuário e sanitizar dados para evitar injeção e código.
