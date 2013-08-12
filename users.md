---
layout: main
title: Usuários
---

## Usuários

A API de usuários permite criar, atualizar e desativar usuários.

- [Criar um usuário](#create)
- [Listar todos usuários](#index)
- [Listar um usuário específico](#show)
- [Atualizar um usuário](#update)

### <a name="create">Criar um usuário</a>

	POST /users HTTP/1.1
	Content-Type: "application/json"
	Accept: "application/json"

**Requisição** *(Todos os parâmetros são obrigatórios)*

	{
		"email": "foobar@example.com",
		"name": "Foo Bar",
		"password": "password"
	}

**Resposta**

	{
		"id": "1",
		"email": "foobar@example.com",
		"name": "Foo Bar",
		"created_at": "2013-07-23 19:39:22",
		"updated_at": "2013-07-23 19:39:22",
	}

### <a name="index">Listar todos usuários</a>

	GET /users HTTP/1.1
	Content-Type: "application/json"
	Accept: "application/json"

**Resposta:**

	[
		{
			"id": "1",
			"email": "foobar@example.com",
			"name": "Foo Bar",
			"created_at": "2013-07-23 19:39:22",
			"updated_at": "2013-07-23 19:39:22"
		},{
			"id": "2",
			"email": "lorem@ipsum.com",
			"name": "Lorem Ipsum",
			"created_at": "2013-07-23 19:39:22",
			"updated_at": "2013-07-23 19:39:22"
		}
	]

### <a name="show">Listar um usuário específico</a>

	GET /users?email=foobar@example.com HTTP/1.1
	Content-Type: "application/json"
	Accept: "application/json"

**Resposta:**

	{
		"id": "1",
		"email": "foobar@example.com",
		"name": "Foo Bar",
		"created_at": "2013-07-23 19:39:22",
		"updated_at": "2013-07-23 19:39:22"
	}

### <a name="update">Atualizar um usuário</a>

	PUT /users?email=foobar@example.com HTTP/1.1
	Content-Type: "application/json"
	Accept: "application/json"

**Requisição** *(Todos os parâmetros são opcionais, basta passar os que quiser atualizar
)*

	{
		"email": "foobar_new_email@example.com",
		"name": "New Name",
		"password": "newpassword"
	}

**Resposta**

	{
		"id": "1",
		"email": "foobar_new_email@example.com",
		"name": "New Name",
		"created_at": "2013-07-23 19:39:22",
		"updated_at": "2013-07-23 19:39:22"
	}