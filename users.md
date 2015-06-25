---
layout: main
title: Usuários
nav:
    - text: "Criar um usuário"
      href: "#create"
    - text: "Listar todos usuários"
      href: "#index"
    - text: "Exibir um usuário específico"
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

    POST /account/users HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

**Requisição** *(Todos os parâmetros são obrigatórios, exceto password)*

    {
        "email": "foobar@example.com",
        "name": "Foo Bar",
        "password": "password"
    }

**Resposta**

    {
        "username": "foobar",
        "name": "foobar",
        "email": "foobar@example.com",
        "updated_at": {
            "date": "2015-06-24 18:58:39.000000",
            "timezone_type": 3,
            "timezone": "UTC"
        },
        "created_at": {
            "date": "2015-06-24 18:58:39.000000",
            "timezone_type": 3,
            "timezone": "UTC"
        },
        "id": 34934,
        "status": {
            "value": "enabled",
            "created_at": {
                "date": "2015-06-24 18:58:39.000000",
                "timezone_type": 3,
                "timezone": "UTC"
            }
        }
    }

### <a id="index">Listar todos usuários</a>

    GET /account/users HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

**Resposta:**

    [
        {
            "id": 34928,
            "email": "barfoo@example.com",
            "username": "barfoo",
            "name": "barfoo",
            "about": null,
            "avatar_filename": null,
            "avatar_height": "300",
            "avatar_width": "300",
            "activity_at": "2015-06-24 17:56:44",
            "activity_count": 3183,
            "created_at": "2015-01-30 21:36:41",
            "updated_at": "2015-06-24 18:43:51",
            "status": {
                "value": "enabled",
                "created_at": "2015-01-30 21:37:13"
            }
        },
        {
            "id": 34934,
            "email": "foobar@example.com",
            "username": "foobar",
            "name": "foobar",
            "about": null,
            "avatar_filename": null,
            "avatar_height": "300",
            "avatar_width": "300",
            "activity_at": null,
            "activity_count": 0,
            "created_at": "2015-06-24 18:58:39",
            "updated_at": "2015-06-24 18:58:39",
            "status": {
                "value": "enabled",
                "created_at": "2015-06-24 18:58:39"
            }
        }
    ]

### <a id="show">Exibir um usuário específico</a>

    GET /account/users/:id HTTP/1.1
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

    PUT /account/users/:id HTTP/1.1
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

    POST /account/users/:id/disable HTTP/1.1
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

    POST /account/users/:id/enable HTTP/1.1
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
