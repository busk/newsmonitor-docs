---
layout: main
title: Usuários
nav:
    - text: "Criar um usuário"
      href: "#create"
    - text: "Listar todos usuários"
      href: "#index"
    - text: "Listar um usuário específico"
      href: "#show"
    - text: "Atualizar um usuário"
      href: "#update"
    - text: "Desativar um usuário"
      href: "#disable"
    - text: "Ativar um usuário"
      href: "#enable"
---

## Usuários

A API de usuários permite criar, atualizar e desativar usuários.

### <a id="create">Criar um usuário</a>

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
        "id": "467",
        "email": "foobar@example.com",
        "name": "Foo Bar",
        "created_at": "2013-07-23 19:39:22",
        "updated_at": "2013-07-23 19:39:22",
    }

### <a id="index">Listar todos usuários</a>

    GET /users HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

**Resposta:**

    [
        {
            "id": "467",
            "email": "foobar@example.com",
            "name": "Foo Bar",
            "created_at": "2013-07-23 19:39:22",
            "updated_at": "2013-07-23 19:39:22"
        },{
            "id": "468",
            "email": "lorem@ipsum.com",
            "name": "Lorem Ipsum",
            "created_at": "2013-07-23 19:39:22",
            "updated_at": "2013-07-23 19:39:22"
        }
    ]

### <a id="show">Listar um usuário específico</a>

    GET /users/:id HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

**Resposta:**

    {
        "id": "467",
        "email": "foobar@example.com",
        "name": "Foo Bar",
        "created_at": "2013-07-23 19:39:22",
        "updated_at": "2013-07-23 19:39:22"
    }

### <a id="update">Atualizar um usuário</a>

    PUT /users/:id HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

**Requisição** *(Todos os parâmetros são opcionais, basta passar os que quiser atualizar)*

    {
        "email": "foobar_new_email@example.com",
        "name": "New Name",
        "password": "newpassword"
    }

**Resposta**

    {
        "id": "467",
        "email": "foobar_new_email@example.com",
        "name": "New Name",
        "created_at": "2013-07-23 19:39:22",
        "updated_at": "2013-07-23 19:39:22"
    }

### <a id="disable">Desativar um usuário</a>

    POST /users/:id/disable HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

**Resposta**

    {
        "id": "9472",
        "user_id": "467",
        "value": "disabled",
        "created_at": "2013-07-23 19:39:22",
        "updated_at": "2013-07-23 19:39:22"
    }

### <a id="enable">Ativar um usuário</a>

    POST /users/:id/enable HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

**Resposta**

    {
        "id": "9473",
        "user_id": "467",
        "value": "enabled",
        "created_at": "2013-07-23 19:39:22",
        "updated_at": "2013-07-23 19:39:22"
    }
