---
layout: main
title: Introdução
---

# Introdução

Essa é uma versão simplificada da documentação da API.

## URL

As urls para acesso à API são:

**Produção** (utiliza https)

> https://newsmonitor.com.br/api/

**Sandbox** (**não** utiliza https)

> http://staging.newsmonitor.com.br/api/

## Headers

A API suporta somente JSON mas pode suportar outros padrões no futuro.<br />
Recomendamos que utilize os seguinte headers:

	"Content-Type": "application/json"
	"Accept": "application/json"

## Autenticação

Para autenticação na API, você deve utilizar HTTP Basic. Sendo o user seu `public_token` e o password o seu `private_token`.  O header da requisição deve conter o seguinte valor:

	"Authorization": "Basic " + BASE64(PUBLIC_TOKEN + ":" + PRIVATE_TOKEN)

Exemplo de autenticação usando o curl em PHP.

	$ch = curl_init();
	curl_setopt($ch, CURLOPT_USERPWD, $public_token . ":" . $private_token;
