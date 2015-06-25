---
layout: main
title: Introdução
nav:
    - text: "URL"
      href: "#url"
    - text: "Autenticação"
      href: "#auth"
---

## Introdução

Essa é uma versão simplificada da documentação da API.

### <a id="url">URL</a>

`https://newsmonitor.com.br/api/v1/`

**Atenção:** Para a segurança de nossos clientes, a API do NewsMonitor requer o uso do protocolo HTTPS. 

### <a id="auth">Autenticação</a>

A autenticação na API utiliza o padrão HTTP Basic.

Exemplo de autenticação em HTTP:

    GET https://newsmonitor.com.br/api/v1/ HTTP/1.1
    Authorization: "Basic " + BASE64(TOKEN + ":")

Exemplo de autenticação usando o CURL em PHP:

    curl_setopt($ch, CURLOPT_HTTPAUTH, CURLAUTH_BASIC);
    curl_setopt($ch, CURLOPT_USERPWD, $token . ":");