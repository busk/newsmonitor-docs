---
layout: main
title: Single Sign On
---

## Single Sign On

- [Criar um token](#create)
- [Redirecionado o usuário](#redirect)
- [Exemplo em PHP](#example)

### <a name="create">Criar um token</a>

O primeiro passo para utilização de SSO é requisitar um token encriptado na API do NewsMonitor.

	POST /token HTTP/1.1

**Requisição**

	{
		"email": "foobar@example.com"
	}

**Resposta**

	{
		"token": "l2kkbESbP9QnUnxnxd9pCTQFAKck4SaIgRUdZhmCsHmMyVsz0DHdfIlJwJZXneEpYMaMI+MAl9+RGA2YH5zomfhWxGUbrvZefKsnmI+PmhKr/OqBN8LwVdq0ZGQjKUA0"
	}

### <a name="redirect">Redirecionado o usuário</a>

Com o token em mãos, o cliente redireciona o usuário para a página de login, passando o token emitido como parâmetro:

    GET /auth/login?token=TOKEN HTTP/1.1

### <a name="example">Exemplo em PHP</a>
