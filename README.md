## Une API c'est quoi ?

Une API (application programming interface ou interface de programmation applicative en français) est un ensemble normalisé de classes, de méthodes, de fonctions et de constantes qui sert de façade par laquelle un logiciel offre des services à d'autres logiciels. Elle est offerte par une bibliothèque logicielle ou un service web.

On parle d'API à partir du moment où une entité informatique cherche à agir avec ou sur un système tiers et que cette interaction se fait de manière normalisée en respectant les contraintes d'accès définies par le système tiers. On dit alors que le système tiers « expose une API ».

Attention, **une API n'est pas toujours un service web**. Malgré l'abus de language qui vise à dire qu'une API est lié au web pour la récupération des données, nous retrouvons des API dans d'autres contextes, comme les références API des languages ou bibliothèques.

Ceci est une API mais service web:

- [https://cat-fact.herokuapp.com/facts](https://cat-fact.herokuapp.com/facts)

Ceci est aussi une API mais de référence logielle:

- [https://laravel.com/api/master/index.html](https://laravel.com/api/master/index.html)

## REST c'est quoi ?

REST est un acronyme pour REpresentational State Transfer et un style architectural pour les systèmes hypermédias distribués.

REST n'est pas un protocole ou une norme, **c'est un style architectural**. Au cours de la phase de développement, les développeurs d'API peuvent **mettre en œuvre REST de différentes manières**.

Comme les autres styles architecturaux, REST a aussi ses principes directeurs et ses contraintes. Ces principes doivent être respectés pour qu'une interface de service puisse être qualifiée de RESTful.

Une API (ou un service web) conforme au style architectural REST est appelée API REST (ou API RESTful).

REST définit 6 contraintes architecturales qui font de tout service web une véritable API RESTful.

- Uniform interface
- Client-server
- Stateless
- Cacheable
- Layered system
- Code on demand (optional)

## REST chez Glanum

Même si il est de notre devoir de suivre au mieux les  contraintes architecturales REST, elles ne peuvent pas toutes toujours être respectées à la lettre.
L'architecture logicielle étant aussi un jeu de compromis, toutes ces contraintes ne seront pas implémentées parfaitement. De plus, la définition de REST précise que les développeurs peuvent choisir la mise en oeuvre de REST.
Nos API suivrons REST mais **ne seront pas RESTful**.

## Structure du projet

Le structure du projet prend exemple sur le domain driven design sans pour autant en faire une implémentation intégrale.

Le répertoire `app` représente l'application et ses points d'entrés (Routing, Validations, Middlewares Controllers...).
Le répertoire `domains` contient toutes les classes répondant directement aux règles métier du client (Models, Repositories...)
Le répertoire `core` contient des outils généraux qui n'implémentent pas directement les règles métier du client mais utiles à ces dernières (Classe de génération de PDF). 

Les reste des répertoires conservents leurs fonctionnements liés à Laravel.

## Sources

- [https://fr.wikipedia.org/wiki/Interface_de_programmation](https://fr.wikipedia.org/wiki/Interface_de_programmation)
- [https://restfulapi.net/rest-architectural-constraints](https://restfulapi.net/rest-architectural-constraints)

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.
