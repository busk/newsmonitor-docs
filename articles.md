---
layout: main
title: Artigos
nav:
    - text: "Mais publicados"
      href: "#most_published"
    - text: "Mais compartilhados"
      href: "#most_shared"
    - text: "Recomendados"
      href: "#recommended"
---

## Artigos

### <a id="most_published">Mais publicados</a>

    GET /articles/most_published/:LANGUAGE HTTP/1.1
    Content-Type: "application/json"
    Accept: "application/json"

**Parâmetros**

-  `LANGUAGE` *(opcional)*
    - `pt` para Português *(valor padrão)*
    - `en` para Inglês
    - `es` para Espanhol

**Resposta**

    [
        {
            "articles": [
                {
                    "id": 172629905,
                    "created_at": "2015-06-25T12:30:30+00:00",
                    "type": "articles",
                    "title": "Luan Santana dedica show em Aracaju ao amigo Cristiano Araújo",
                    "language_code": "pt",
                    "url": "http://g1.globo.com/se/sergipe/sao-joao/2015/noticia/2015/06/luan-santana-dedica-show-em-aracaju-ao-amigo-cristiano-araujo.html",
                    "published_at": "2015-06-25T11:57:35+00:00",
                    "directories": [
                        "Entretenimento",
                        "Cotidiano"
                    ],
                    "publishings": [
                        {
                            "id": 2,
                            "permalink": "g1",
                            "name": "G1",
                            "published_at": "2015-06-25T11:57:35+00:00",
                            "thumbnail": "b23b85d2212c4fdca994.png",
                            "thumbnail_url": "https://s3.amazonaws.com/spixdiscovery/sites/2/favicon/large_b23b85d2212c4fdca994.png",
                            "url": "http://g1.globo.com/"
                        }
                    ],
                    "images": [
                        {
                            "url": "2c0518151a105634e43a8461b5177d39.jpg",
                            "full_url": {
                                "original": "https://d2b3jslbjwb14v.cloudfront.net/assets/feed_item_data/original/2c0518151a105634e43a8461b5177d39.jpg",
                                "300x": "https://d2b3jslbjwb14v.cloudfront.net/assets/feed_item_data/card_300x/2c0518151a105634e43a8461b5177d39.jpg"
                            },
                            "width": 620,
                            "height": 465
                        }
                    ],
                    "social_metrics": {
                        "facebook_likes": 9164,
                        "facebook_shares": 653,
                        "facebook_comments": 181,
                        "facebook_total": 9998,
                        "twitter": 575,
                        "pinterest": 0,
                        "linkedin": 0,
                        "google_plusones": 3
                    },
                    "topics": [
                        {
                            "id": 22201,
                            "name": "luan santana",
                            "label": "Luan Santana",
                            "score": 0.58296251296997
                        },
                        {
                            "id": 7647,
                            "name": "aracaju",
                            "label": "Aracaju",
                            "score": 0.21697092056274
                        },
                        {
                            "id": 8971,
                            "name": "cantor",
                            "label": "Cantor",
                            "score": 0.11585091799498
                        },
                        {
                            "id": 23104,
                            "name": "santana",
                            "label": "Santana",
                            "score": 0.097482040524483
                        },
                        {
                            "id": 35654,
                            "name": "morre",
                            "label": "Morre",
                            "score": 0.090568758547306
                        },
                        {
                            "id": 67278,
                            "name": "forró",
                            "label": "Forró",
                            "score": 0.087043382227421
                        },
                        {
                            "id": 8101,
                            "name": "sertanejo",
                            "label": "Sertanejo",
                            "score": 0.084786415100098
                        },
                        {
                            "id": 29583,
                            "name": "junho",
                            "label": "Junho",
                            "score": 0.061619214713573
                        },
                        {
                            "id": 1929,
                            "name": "cristianismo",
                            "label": "Cristianismo",
                            "score": 0.060725565999746
                        },
                        {
                            "id": 67339,
                            "name": "fãs",
                            "label": "FÃS",
                            "score": 0.05726620182395
                        }
                    ],
                    "videos": []
                }
            ],
            "clusterId": 172407593,
            "clusterSize": 1570,
            "score": 1051.7475585938
        }
    ]

### <a id="most_shared">Mais compartilhados</a>

    GET /articles/most_shared/:LANGUAGE HTTP/1.1 
    Content-Type: "application/json"
    Accept: "application/json"

**Parâmetros**

-  `LANGUAGE` *(opcional)*
    - `pt` para Português *(valor padrão)*
    - `en` para Inglês
    - `es` para Espanhol

***Resposta***

    [
        {
            "articles": [
                {
                    "id": 172537913,
                    "created_at": "2015-06-24T21:48:32+00:00",
                    "type": "articles",
                    "title": "Eliana compra passagem para desempregado em aeroporto no Rio",
                    "language_code": "pt",
                    "url": "http://ego.globo.com/famosos/noticia/2015/06/eliana-compra-passagem-para-desempregado-em-aeroporto-no-rio.html",
                    "published_at": "2015-06-24T21:33:58+00:00",
                    "directories": [
                        "Celebridades"
                    ],
                    "publishings": [
                        {
                            "id": 11289,
                            "permalink": "ego",
                            "name": "Ego",
                            "published_at": "2015-06-24T21:33:58+00:00",
                            "thumbnail": "3mY8ZA8KI5x26jlZIufBcuPZG3Y1tWeZ0HCpRckd.png",
                            "thumbnail_url": "https://s3.amazonaws.com/spixdiscovery/sites/11289/favicon/large_3mY8ZA8KI5x26jlZIufBcuPZG3Y1tWeZ0HCpRckd.png",
                            "url": "http://ego.globo.com/"
                        }
                    ],
                    "images": [
                        {
                            "url": "0a9484990fde78e3c4a9e973059222a8.jpg",
                            "full_url": {
                                "original": "https://d2b3jslbjwb14v.cloudfront.net/assets/feed_item_data/original/0a9484990fde78e3c4a9e973059222a8.jpg",
                                "300x": "https://d2b3jslbjwb14v.cloudfront.net/assets/feed_item_data/card_300x/0a9484990fde78e3c4a9e973059222a8.jpg"
                            },
                            "width": 620,
                            "height": 436
                        }
                    ],
                    "social_metrics": {
                        "facebook_likes": 80577,
                        "facebook_shares": 2673,
                        "facebook_comments": 3128,
                        "facebook_total": 86378,
                        "twitter": 292,
                        "pinterest": 0,
                        "linkedin": 0,
                        "google_plusones": 3
                    },
                    "topics": [
                        {
                            "id": 37951,
                            "name": "eliana",
                            "label": "Eliana",
                            "score": 0.28975474834442
                        },
                        {
                            "id": 5921,
                            "name": "aeroportos",
                            "label": "Aeroportos",
                            "score": 0.085999526083469
                        },
                        {
                            "id": 24767,
                            "name": "fátima bernardes",
                            "label": "Fátima Bernardes",
                            "score": 0.072233207523823
                        },
                        {
                            "id": 10691,
                            "name": "voo",
                            "label": "VOO",
                            "score": 0.066829681396484
                        },
                        {
                            "id": 25606,
                            "name": "guarulhos",
                            "label": "Guarulhos",
                            "score": 0.06146352365613
                        },
                        {
                            "id": 9874,
                            "name": "débora nascimento",
                            "label": "Débora Nascimento",
                            "score": 0.059866089373827
                        },
                        {
                            "id": 29438,
                            "name": "adriane galisteu",
                            "label": "Adriane Galisteu",
                            "score": 0.058381229639053
                        },
                        {
                            "id": 10914,
                            "name": "rodrigo faro",
                            "label": "Rodrigo Faro",
                            "score": 0.052441451698542
                        },
                        {
                            "id": 32409,
                            "name": "p&b",
                            "label": "P&B",
                            "score": 0.050602212548256
                        }
                    ],
                    "videos": []
                }
            ],
            "clusterId": 172501988,
            "clusterSize": 22,
            "score": 83545
        }
    ]


### <a id="recommended">Recomendados</a>

    GET /articles/recommended/ HTTP/1.1 
    Content-Type: "application/json"
    Accept: "application/json"

***Resposta***
    
    [
        {
            "articles": [
                {
                    "id": 172629905,
                    "created_at": "2015-06-25T12:30:30+00:00",
                    "type": "articles",
                    "title": "Luan Santana dedica show em Aracaju ao amigo Cristiano Araújo",
                    "language_code": "pt",
                    "url": "http://g1.globo.com/se/sergipe/sao-joao/2015/noticia/2015/06/luan-santana-dedica-show-em-aracaju-ao-amigo-cristiano-araujo.html",
                    "published_at": "2015-06-25T11:57:35+00:00",
                    "directories": [
                        "Entretenimento",
                        "Cotidiano"
                    ],
                    "publishings": [
                        {
                            "id": 2,
                            "permalink": "g1",
                            "name": "G1",
                            "published_at": "2015-06-25T11:57:35+00:00",
                            "thumbnail": "b23b85d2212c4fdca994.png",
                            "thumbnail_url": "https://s3.amazonaws.com/spixdiscovery/sites/2/favicon/large_b23b85d2212c4fdca994.png",
                            "url": "http://g1.globo.com/"
                        }
                    ],
                    "images": [
                        {
                            "url": "2c0518151a105634e43a8461b5177d39.jpg",
                            "full_url": {
                                "original": "https://d2b3jslbjwb14v.cloudfront.net/assets/feed_item_data/original/2c0518151a105634e43a8461b5177d39.jpg",
                                "300x": "https://d2b3jslbjwb14v.cloudfront.net/assets/feed_item_data/card_300x/2c0518151a105634e43a8461b5177d39.jpg"
                            },
                            "width": 620,
                            "height": 465
                        }
                    ],
                    "social_metrics": {
                        "facebook_likes": 9164,
                        "facebook_shares": 653,
                        "facebook_comments": 181,
                        "facebook_total": 9998,
                        "twitter": 575,
                        "pinterest": 0,
                        "linkedin": 0,
                        "google_plusones": 3
                    },
                    "topics": [
                        {
                            "id": 22201,
                            "name": "luan santana",
                            "label": "Luan Santana",
                            "score": 0.58296251296997
                        },
                        {
                            "id": 7647,
                            "name": "aracaju",
                            "label": "Aracaju",
                            "score": 0.21697092056274
                        },
                        {
                            "id": 8971,
                            "name": "cantor",
                            "label": "Cantor",
                            "score": 0.11585091799498
                        },
                        {
                            "id": 23104,
                            "name": "santana",
                            "label": "Santana",
                            "score": 0.097482040524483
                        },
                        {
                            "id": 35654,
                            "name": "morre",
                            "label": "Morre",
                            "score": 0.090568758547306
                        },
                        {
                            "id": 67278,
                            "name": "forró",
                            "label": "Forró",
                            "score": 0.087043382227421
                        },
                        {
                            "id": 8101,
                            "name": "sertanejo",
                            "label": "Sertanejo",
                            "score": 0.084786415100098
                        },
                        {
                            "id": 29583,
                            "name": "junho",
                            "label": "Junho",
                            "score": 0.061619214713573
                        },
                        {
                            "id": 1929,
                            "name": "cristianismo",
                            "label": "Cristianismo",
                            "score": 0.060725565999746
                        },
                        {
                            "id": 67339,
                            "name": "fãs",
                            "label": "FÃS",
                            "score": 0.05726620182395
                        }
                    ],
                    "videos": []
                }
            ],
            "clusterId": 172407593,
            "clusterSize": 1585,
            "score": 2685.0300292969
        }
    ]