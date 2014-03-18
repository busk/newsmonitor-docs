---
layout: main
title: Introdução
---

## Introdução

Essa é uma versão simplificada da documentação da API.

### <a name="url">URL</a>

`https://newsmonitor.com.br/api/`

**Atenção:** Para a segurança de nossos clientes, a API do NewsMonitor requer o uso do protocolo HTTPS. Caso esteja tendo problemas com nossos certificados, verifique se seu cliente HTTP está utilizando SSL v3.

    curl_setopt($ch, CURLOPT_SSLVERSION, 3);

Se o problema persistir, recomendamos que atualize os certificados em seu servidor.

    $ sudo update-ca-certificates

### <a name="auth">Autenticação</a>

A autenticação na API utiliza o padrão HTTP Basic, sendo o user seu `public_token` e o password seu `private_token`.

Exemplo de autenticação em HTTP:

    GET https://newsmonitor.com.br/api/ HTTP/1.1
    Authorization: "Basic " + BASE64(PUBLIC_TOKEN + ":" + PRIVATE_TOKEN)

Exemplo de autenticação usando o CURL em PHP:

    curl_setopt($ch, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
    curl_setopt($ch, CURLOPT_USERPWD, $public_token . ":" .$private_token);
