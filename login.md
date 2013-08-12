---
layout: main
title: Login
---

## Login

A Api de Login permite autenticar um usuário no NewsMonitor sem que ele precise digitar seu email e senha. O primeiro passo para utilização do login integrado é requisitar um token encriptado do NewsMonitor.


- [Criar um token](#create)
- [Redirecionado o usuário](#redirect)
- [Exemplo em PHP](#example)

### <a name="create">Criar um token</a>

	POST /token HTTP/1.1

**Requisição**

	{
		"email": "foobar@example.com"
	}

**Resposta**

	{
		"token": "ckJmZHNhMTM3NjMzMzcxOGI1aDRMS2MxNjZkbkZLVDE="
	}

### <a name="redirect">Redirecionado o usuário</a>

Com o token em mãos, o cliente redireciona o usuário para a página de login, passando o token emitido como parâmetro:

    HTTP/1.1 302 Found
    Location: https://newsmonitor.com.br/auth/token/TOKEN

### <a name="example">Exemplo completo em PHP</a>

    // obtains token
    $url = 'https://newsmonitor.com.br/api/token?' . http_build_query(array('email' => 'foobar@example.com'));
    
    $ch = curl_init();
    curl_setopt($ch, CURLOPT_URL, $url);
    curl_setopt($ch, CURLOPT_SSLVERSION, 3);
    curl_setopt($ch, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
    curl_setopt($ch, CURLOPT_USERPWD, $public_token . ":" .$private_token);
    curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
    
    $data = json_decode(curl_exec($ch));
    curl_close($ch);
    
    // redirects the user
    http_redirect('https://newsmonitor.com/auth/token/' . $data['token']);

