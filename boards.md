---
layout: main
title: Pastas
nav:
    - text: "Listar as pasta do usuário"
      href: "#index"
    - text: "Criar uma pasta"
      href: "#create"
    - text: "Exibir uma pasta"
      href: "#show"
    - text: "Editar uma pasta"
      href: "#edit"
    - text: "Listar as notícias de uma pasta"
      href: "#index_articles"
    - text: "Listar as permissões de uma pasta"
      href: "#index_permissions"
    - text: "Exibir uma permissão de uma pasta"
      href: "#show_permission"
    - text: "Deletar uma permissão de uma pasta"
      href: "#delete_permission"
    - text: "Adicionar permissão para um usuário na pasta"
      href: "#add_permission"
    - text: "Atualizar permissões da pasta"
      href: "#update_permission"
---

## Pastas

### <a id="index">Listar as pasta do usuário</a>

    GET /boards HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

**Resposta**

    [
        {
            "id": 54,
            "title": "lorem",
            "permalink": "lorem",
            "description": null,
            "privacy": "private",
            "created_at": "2015-03-13T17:48:47+00:00",
            "updated_at": "2015-03-13T17:48:47+00:00",
            "permissions": [
                {
                    "id": 23,
                    "user_id": 34928,
                    "is_owner": true,
                    "unseen_articles_count": 0,
                    "last_viewed_at": "2015-06-22T18:51:47+00:00",
                    "created_at": "2015-03-13T17:48:47+00:00",
                    "updated_at": "2015-06-22T18:51:47+00:00"
                }
            ]
        },
        {
            "id": 55,
            "title": "ipsum",
            "permalink": "ipsum",
            "description": null,
            "privacy": "private",
            "created_at": "2015-03-16T14:44:43+00:00",
            "updated_at": "2015-03-16T14:44:43+00:00",
            "permissions": [
                {
                    "id": 223,
                    "user_id": 34928,
                    "is_owner": true,
                    "unseen_articles_count": 0,
                    "last_viewed_at": null,
                    "created_at": "2015-03-16T14:44:43+00:00",
                    "updated_at": "2015-03-16T14:44:43+00:00"
                }
            ]
        }
    ]

### <a id="create">Criar uma pasta</a>

    POST /boards HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

***Requisição*** *(Apenas o parâmetro `title` é obrigatório)*

    {
        "title": "Title",
        "description": "Description",
        "privacy": "private" | "public" | "organization"
    }

***Resposta***

    {
        "id": 84,
        "title": "Title",
        "permalink": "title",
        "description": null,
        "privacy": "private",
        "created_at": "2015-03-13T17:48:47+00:00",
        "updated_at": "2015-06-24T21:01:10+00:00",
        "permissions": [
            {
                "id": 23,
                "user_id": 34928,
                "is_owner": true,
                "unseen_articles_count": 0,
                "last_viewed_at": "2015-06-22T18:51:47+00:00",
                "created_at": "2015-03-13T17:48:47+00:00",
                "updated_at": "2015-06-22T18:51:47+00:00"
            }
        ]
    }

### <a id="show">Exibir uma pasta</a>

    GET /boards/:ID HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

***Resposta***
    
    {
        "id": 54,
        "title": "lorem",
        "permalink": "lorem",
        "description": null,
        "privacy": "private",
        "created_at": "2015-03-13T17:48:47+00:00",
        "updated_at": "2015-03-13T17:48:47+00:00",
        "permissions": [
            {
                "id": 23,
                "user_id": 34928,
                "is_owner": true,
                "unseen_articles_count": 0,
                "last_viewed_at": "2015-06-22T18:51:47+00:00",
                "created_at": "2015-03-13T17:48:47+00:00",
                "updated_at": "2015-06-22T18:51:47+00:00"
            }
        ]
    }

### <a id="edit">Editar uma pasta</a>

    PUT /boards/:ID HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

***Requisição*** *(Todos os parâmetros são opcionais, basta passar os que quiser atualizar)*

    {
        "title": "Title",
        "description": "Description",
        "privacy": "private" | "public" | "organization"
    }

***Resposta***

    {
        "id": 54,
        "title": "lorem",
        "permalink": "lorem",
        "description": "Add description",
        "privacy": "private",
        "created_at": "2015-03-13T17:48:47+00:00",
        "updated_at": "2015-03-13T17:48:47+00:00",
        "permissions": [
            {
                "id": 23,
                "user_id": 34928,
                "is_owner": true,
                "unseen_articles_count": 0,
                "last_viewed_at": "2015-06-22T18:51:47+00:00",
                "created_at": "2015-03-13T17:48:47+00:00",
                "updated_at": "2015-06-22T18:51:47+00:00"
            }
        ]
    }

### <a id="index_articles">Listar as notícias de uma pasta</a>

    GET /boards/:ID/articles HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

***Resposta***

    [
        {
            "id": 1855,
            "board_id": 54,
            "article_id": 154909879,
            "user_id": 34928,
            "description": "",
            "created_at": "2015-06-25T13:55:08+00:00",
            "updated_at": "2015-06-25T13:55:08+00:00",
            "article": {
                "id": 154909879,
                "created_at": "2015-03-23T17:20:38+00:00",
                "type": "articles",
                "title": "Pillars of Eternity video reveals the pressures of Kickstarter success",
                "language_code": "en",
                "url": "http:\\/\\/www.pcgamer.com\\/pillars-of-eternity-video-reveals-the-pressures-of-kickstarter-success\\/",
                "published_at": "2015-03-23T17:13:47+00:00",
                "directories": [
                    "Games"
                ],
                "publishings": [
                    {
                        "id": 12122,
                        "permalink": "pc-gamer",
                        "name": "PC Gamer",
                        "published_at": "2015-03-23T17:13:47+00:00",
                        "thumbnail": "ry50kF16tPcTqVyitGYOHxLTeAoyrH5HuJATu98o.png",
                        "thumbnail_url": "https:\\/\\/s3.amazonaws.com\\/spixdiscovery\\/sites\\/12122\\/favicon\\/large_ry50kF16tPcTqVyitGYOHxLTeAoyrH5HuJATu98o.png",
                        "url": "http:\\/\\/www.pcgamer.com"
                    }
                ],
                "images": [
                    {
                        "url": "f1923cd73387830200f8587e645a025f.jpg",
                        "full_url": {
                            "original": "https:\\/\\/d2b3jslbjwb14v.cloudfront.net\\/assets\\/feed_item_data\\/original\\/f1923cd73387830200f8587e645a025f.jpg",
                            "300x": "https:\\/\\/d2b3jslbjwb14v.cloudfront.net\\/assets\\/feed_item_data\\/card_300x\\/f1923cd73387830200f8587e645a025f.jpg"
                        },
                        "width": 1200,
                        "height": 630
                    }
                ],
                "social_metrics": {
                    "facebook_likes": 3,
                    "facebook_shares": 9,
                    "facebook_comments": 1,
                    "facebook_total": 13,
                    "twitter": 38,
                    "pinterest": 0,
                    "linkedin": 0,
                    "google_plusones": 0
                },
                "topics": [
                    {
                        "id": 44006,
                        "name": "obsidian",
                        "label": "Obsidian",
                        "score": 0.27268105745316
                    },
                    {
                        "id": 58870,
                        "name": "obsidian entertainment",
                        "label": "Obsidian Entertainment",
                        "score": 0.12668016552925
                    },
                    {
                        "id": 56221,
                        "name": "project eternity",
                        "label": "Project Eternity",
                        "score": 0.12605433166027
                    },
                    {
                        "id": 35096,
                        "name": "fallout",
                        "label": "Fallout",
                        "score": 0.054113369435072
                    },
                    {
                        "id": 3539,
                        "name": "lucasarts",
                        "label": "Lucasarts",
                        "score": 0.050601676106453
                    }
                ],
                "videos": [
                    {
                        "url": "http:\\/\\/youtube.com\\/watch?v=iBR6TOdb73g",
                        "thumb_filename": "de41372c300ec6d5ad88f5cd86dae799.jpg",
                        "thumb_width": 320,
                        "thumb_height": 180
                    }
                ]
            },
            "author": {
                "id": 34928,
                "email": "barfoo@example.com",
                "username": "barfoo",
                "name": "barfoo",
                "about": null,
                "avatar_filename": null,
                "avatar_height": "300",
                "avatar_width": "300",
                "activity_at": "2015-06-25T13:55:04+00:00",
                "activity_count": 3233,
                "created_at": "2015-01-30T21:36:41+00:00",
                "updated_at": "2015-06-25T13:52:46+00:00"
            },
            "comments": []
        }
    ]

### <a id="index_permissions">Listar as permissões de uma pasta</a>

    GET /boards/:ID/permissions HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json

***Resposta***
    
    [
        {
            "id": 23,
            "user_id": 34928,
            "is_owner": true,
            "unseen_articles_count": 0,
            "last_viewed_at": "2015-06-29T20:13:33+00:00",
            "created_at": "2015-03-13T17:48:47+00:00",
            "updated_at": "2015-06-29T20:13:33+00:00"
        }
    ]

### <a id="show_permission">Exibir uma permissão de uma pasta</a>

    GET /boards/:ID/permissions/:ID HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json

***Resposta***

    {
        "id": 23,
        "user_id": 34928,
        "is_owner": true,
        "unseen_articles_count": 0,
        "last_viewed_at": "2015-06-29T20:13:33+00:00",
        "created_at": "2015-03-13T17:48:47+00:00",
        "updated_at": "2015-06-29T20:13:33+00:00"
    }

### <a id="delete_permission">Deletar uma permissão de uma pasta</a>

    DELETE /boards/:ID/permissions/:ID HTTP/1.1 (Não é possível deletar a permissão do Owner)
    Content-Type: "application/json"
    Accept: "application/json

***Resposta***

    [
        {
            "id": 24,
            "user_id": 34928,
            "is_owner": true,
            "unseen_articles_count": 0,
            "last_viewed_at": "2015-06-29T20:41:43+00:00",
            "created_at": "2015-03-16T14:44:43+00:00",
            "updated_at": "2015-06-29T20:41:43+00:00"
        }
    ]

### <a id="add_permission">Adicionar permissão para um usuário na pasta</a>
    
    POST /boards/:ID/permissions/ HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json

***Requisição*** *(Apenas para usuários da empresa)*

    {
        "user_id": 34934,
    }

***Resposta***

    [
        {
            "id": 23,
            "user_id": 34928,
            "is_owner": true,
            "unseen_articles_count": 0,
            "last_viewed_at": "2015-06-29T20:13:33+00:00",
            "created_at": "2015-03-13T17:48:47+00:00",
            "updated_at": "2015-06-29T20:13:33+00:00"
        },
        {
            "user_id": 34934,
            "is_owner": false,
            "last_viewed_at": null,
            "unseen_articles_count": 0,
            "updated_at": "2015-06-29T20:49:38+00:00",
            "created_at": "2015-06-29T20:49:38+00:00",
            "id": 66
        }
    ]

### <a id="update_permission">Atualizar permissões da pasta</a>
    
    PUT /boards/:ID/permissions/ HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json

***Requisição*** *(Apenas `user_id`. O Owner não é alterado)*

    {
        "permissions":[
            {
                "user_id": 34938
            }
        ]
    }

***Resposta***

    [
        {
            "id": 23,
            "user_id": 34928,
            "is_owner": true,
            "unseen_articles_count": 0,
            "last_viewed_at": "2015-06-29T20:13:33+00:00",
            "created_at": "2015-03-13T17:48:47+00:00",
            "updated_at": "2015-06-29T20:13:33+00:00"
        },
        {
            "id": 66,
            "user_id": 34934,
            "is_owner": false,
            "last_viewed_at": null,
            "unseen_articles_count": 0,
            "updated_at": "2015-06-29T21:15:04+00:00",
            "created_at": "2015-06-29T21:15:04+00:00"
        },
        {
            "user_id": 34938,
            "is_owner": false,
            "unseen_articles_count": 0,
            "last_viewed_at": null,
            "created_at": "2015-06-29T21:09:46+00:00",
            "updated_at": "2015-06-29T21:09:46+00:00",
            "id": 69
        }
    ]