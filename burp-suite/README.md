# LAB: USERNAME ENUMERATION VIA DIFFERENT RESPONSES (Enumeração de nomes de usuário através de diferentes respostas do servidor)

# Objetivo: O enunciado do LAB trouxe uma lista de possíveis usernames e passwords utilizadas no IP Teste, o objetivo era acessar com usuários e senhas válidos, invadindo através de BURP SUITE.

# Ferramentas usadas:
  1. Portswigger Web Security Academy
  2. BURP Suite Community Edition

# Metodologia:
  1. Identificaçao da página de login (neste caso, página My Account em /login)
  2. Tentativa de login "falso" para capturar a página com POST
  3. Interceptaçao com BURP SUITE na aba Proxy
  4. Marcaçao de tentativa de login atraves de parágrafos (Exemplo: username=§login-errado§&password=tentativa-falsa)
  5. Uso do Intruder do BURP SUITE, copiando para a aba PAYLOAD os possíveis usuários e execuçao de brute-forcing attack
  6. Identificaçao de qual usuário foi aceito pela url
  7. Tentativa de combinaçao usuário-senha para login invasivo com uso de parágrafos novamente (Exemplo: username=login-correto&password=§tentativa-de-invasao§
  8. Identificaçao de usuário e senha compatíveis dentro da aba de resultados
  9. Login e senha identificados no LAB = LAB SOLVED

# Aprendizados: 
Uso das ferramentas PROXY E INTRUDER do BURP SUITE para invasão com usuários e senhas previsíveis
