---
layout: main
title: Login
nav:
    - text: "Criar um token"
      href: "#create"
    - text: "Redirecionado o usuário"
      href: "#redirect"
    - text: "Exemplo em PHP"
      href: "#example"
---

## Login

A Api de Login permite autenticar um usuário no NewsMonitor sem que ele precise digitar seu email e senha. O primeiro passo para utilização do login integrado é requisitar um token encriptado do NewsMonitor.


### <a id="create">Criar um token</a>

    POST /account/users/:ID/token HTTP/1.1
    Accept: "application/json"

**Resposta**

    {
        "token": "REZKZUhhMTQzNTE3NTIyMmJrdmFNamMzNDkzNGRXNmVqQQ=="
    }

### <a id="redirect">Redirecionado o usuário</a>

Com o token em mãos, o cliente redireciona o usuário para a página de login, passando o token emitido como parâmetro:

    HTTP/1.1 302 Found
    Location: https://newsmonitor.com.br/auth/token/TOKEN

### <a id="example">Exemplo completo em PHP</a>

    // obtains token
    $url = 'https://newsmonitor.com.br/api/account/token?' . http_build_query(array('email' => 'foobar@example.com'));
    
    $ch = curl_init();
    curl_setopt($ch, CURLOPT_URL, $url);
    curl_setopt($ch, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
    curl_setopt($ch, CURLOPT_USERPWD, $token . ":");
    curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
    
    $data = json_decode(curl_exec($ch));
    curl_close($ch);
    
    // redirects the user
    http_redirect('https://newsmonitor.com/auth/token/' . $data['token']);

