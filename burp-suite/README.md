# LAB: USERNAME ENUMERATION VIA DIFFERENT RESPONSES
### Enumeração de nomes de usuário através de diferentes respostas do servidor


# Objetivo: O enunciado do LAB trouxe uma lista de possíveis usernames e passwords utilizadas no ambiente de teste. O objetivo era identificar usuários e senhas válidos e, posteriormente, encontrar a combinaçao correta para invasão do ambiente teste através de BURP SUITE.

# Ferramentas usadas:
  1. Portswigger Web Security Academy
  2. BURP Suite Community Edition

# Metodologia:
  1. Identificação da página de login (neste caso, '/login').
  2. Realização de uma tentativa de login inválida para capturar a requisiçao 'POST'.
  3. Interceptação da requisição utilizando a aba **Proxy** do BURP SUITE.
  4. Marcação do parametro 'username' com payload para testar diferentes usuários.
    - Exemplo: username=§login-errado§&password=tentativa-falsa
  5. Utilização do **Intruder** do BURP SUITE para testar a lista de possíveis usernames.
  6. Análise de respostas, mais especificamente a aba Length, para identificar diferenças que apontassem para um username válido.
  7. Após identificar um username válido, marcação do parâmetro 'password' como payload.
    - Exemplo: username=login-correto&password=§tentativa-de-invasao§
  8. Utilização do **Intruder** novamente para testar as possíveis senhas.
  9. Identificação de usuário e senha compatíveis dentro da aba de resultados do Intruder.
  10. Login e senha realizados com sucesso = LAB SOLVED.

# Aprendizados: 
 - Uso das ferramentas PROXY E INTRUDER do BURP SUITE para teste de credenciais em ambiente controlado.
 - Enumeração de usernames através da analise de diferentes respostas do servidor.
 - Identificação de padrões nas respostas de uma aplicação WEB.
