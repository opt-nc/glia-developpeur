## ❔ A propos

Le but de ce document est de fournir un ensemble de questions/réponses permettant
de **mieux cerner les spécificités du poste de Développeur au GLIA.**

## 🧑‍🤝‍🧑 Organsiation du travail et collaboration

- "Est-t-il possible de travailler à distance ?"
- "Oui, à hauteur de 2 jours maximum par semaine et sur des créneaux horaires convenus à l'avance, à l'exceptiondu jeudi après-midi où la présence est sur site est exigée."


- "Pourquoi le jeudi après-midi est-il obligatoire ?"
- "Ce créneau est réservé à l'unique SCRUM hebdomadaire, et aux échanges informels entre les membres de l'équipe ainsi qu'aux sujets d'innovation."

## 🙏 Valeurs de l'équipe

Quelle sont les qualités attendues au sein de l'équipe ?

- **La première qualité attendue est l'esprit d'équipe**, en particulier la capacité à partager ses connaissances afin d'avancer collectivement. En particulier, nous attendons que le logigicel produit puisse être maintenu par n'importe quel membre de l'équipe, durablement et à moindre effort. Nous ne valorisons pas les "héros" qui résolvent des problèmes de manière individuelle, mais les "équipes" qui résolvent des problèmes de manière collective
- **Le sens du client : les bureaux demandeurs de données ou d'interopérabilité** sont nos clients, notre mission est de leur offir la meilleure expérience possible, que ce soit une DevEx (Dévelopeur Experience) ou une data experience (production de métriques inédites par exemple)


## 👐 Déroulé de l'accueil

### 🤔 Lors de ma première semaine que vais-je faire ?

L'équipe du GLIA vous sera présentée, ainsi que les autres bureaux avec lesquels nous sommes en forte collaboration, puis progressivement les autres services de l'office.

Dès la première semaine il vous sera demandé de:

1. **Comprendre la culture du bureau** via le blog : https://dev.to/optnc2.
2. **Comprendre et installer** la cartographie du système d'information : https://dev.to/optnc/our-speech-about-it-holism-at-nodes22-1bpl
3. **Choisir une distribution Linux** pour votre poste de travail, motiver le choix et la faire valider auprès de l'équipe
4. **Prendre en charge un projet d'innovation** qui vous sera proposé et que vous devrez mener à bien de bout en bout, dans le respect des méthodes et outils de l'équipe: ce projet sera votre fil rouge pour votre intégration
5. **Participer** au premier SCRUM et présenter vos avancées


## 🧰 La stack technique

- "Quelle est la stack Java utilisée ?"
- "Nous utilions Maven pour builder, Quarkus pour les microservices et batches, et maintenons des applications Spring Boot historiques... en cours de migration vers Quarkus."


- "Quelle votre base de données relationnelle pour les développements spécifiques?"
- "Nous utilisons PostgreSQL pour les développements spécifiques."


- "Quels sont les outils que je vais devoir installer sur ma workstation?"
- "Tous les outils de build, principalement Maven, Podman et Git, ainsi que les outils de développement Java, IntelliJ IDEA ou VSCode selon vos préférences."


- "Utilisez-vous des containers ?"
- "Oui, systématiquement, pour tout, partout et tout le temps. Nous utilisons Podman pour les containers, et Ansible/Tower pour les déploiements via des GtiHub actions déidées. Tout est systématiquement livré sous forme de containers, en continu via la regisrty ghcr.io de Github.com. Les tests sont également déroulées via des containers."


- "Comment exécutez-vous les containers ?"
- "DEVs et OPs partagent la même stack technique (de bout en bout), et les containers sont exécutés en local via Podman, et en production via Podman pour l'instant. Tout est automatisé via Ansible/Tower."


- "Quels sont les middleware utilisés ?"
- "Le GLIA utilise Kafka (développement de producers, consumers, streams,...) pour les échanges asynchrones, et la haute disponibilité, Open Search pour les recherches full text et les logs, PostgreSQL pour les bases de données relationnelles, consul pour partager des configurations, Neo4J pour la cartographie du SI."


- "Avec quoi buildez-vous vos applications ?"
- "On builde avec Maven, et on teste avec JUnit, TestContainers (et d'autres frameworks cloud-natifs encore en cours d'intégration) via des actions Github et des workflows dédiés"


- Où sont gérées les issues ?
- Les issues de support arrivent via un système de ticket externe que nous avons intégré à Github, et les issues de développement sont gérées via Github. Elles sont totalement liées au processus de build, de déploiement et de maintenance des applications.


- "Quelle CI utilisez-vous ?"
- "Nous utilisons tous les services mis à disposition par Github, et en particulier les actions Github pour les workflows de build, de test, de déploiement, et de maintenance."


- "Commment délivrez-vous vos applications ?"
- "Nous délivrons nos images sur ghcr.io, l'automatication est faite via Ansible/Tower qui vient puller et démarrer les containers sur les serveurs d'intégration, qualification et production. Voir https://github.com/opt-nc/tower-deploy-action"


- "Comment documentez-vous vos APIs ?"
- "Nous développons nos APIs avec Quarkus, nous générons la documentation en continu , notamment avec redocly, cf https://dev.to/optnc/api-documentation-release-automation-with-github-redocly-and-open-api-f6h"


- "Utilisez-vous Kafka ?"
- "Oui, en permanence, Kafka est au coeur de l'ADN du bureau, pour les échanges asynchrones, la haute disponibilité, la scalabilité et l'interopérabilité."


- "Faites-vous de la data science ?"
- "Oui, nous mettons un point d'honneur à décrire les choses avec des données, des APIs,...puis de les valoriser via des applications, des dashboards, des rapports, des analyses, des prédictions, des recommandations, des alertes,... Nous faisons cela avec du Python."


- "Utilisez-vous des bases de données NoSQL ?"
- "Oui, à ce jour de l'OpenSearch, du consul, du Neo4J."


- "Utilisez-vous du Python ?... et si oui, pour quoi faire ?"
- "Oui, pour la datascience, les analyses, des automatisations ou au sein de la CI/CD pour automatiser des traitements, des tests, des déploiements."


- "Sécurisez-vous vos artefacts/images docker... et si oui, comment ?"
- "La sécurité et la dette technique sont au coeur de nos préoccupations. Nous utilisons dependabot pour nous aider et `grype` pour choisir les images de base sur lesquelles nous nous appuyons par la suite, voir : "
-  Par exemple, notre choix pour Kafka https://dev.to/optnc/kafka-image-wurstmeister-vs-bitnami-efg ou encore celui de Java : https://dev.to/optnc/bench-and-choose-java-8-docker-images-with-anchoregrype-4fg8

  
## 🧑‍🚀 Culture de l'innovation

- "J'ai cru comprendre que l'innovation était une valeur forte de l'équipe, comment cela se traduit-il ?"
- "Oui, tout à fait et nous la mettons en oeuvre au quotidien.  Nous sommes adeptes du _"Eating your own dog food"_. Nous mettons un point d'honneur à innover pour pouvoir répondre à des problématiques du quotidien pour nous ou nos clients. Les sujets sont décidés au sein de l'équipe et sont souvent issus de difficultés rencontrées lors du BUILD ou RUN. Les résultats sont systématiquement documentés, démontrés et s'ils ne devaient mener à rien, alors c'est dans un mode de "fail fast" que nous les abandonnons. Le critère de mise à l'échelle de l'innovation est central pour nous."


- "J'ai des compétences en `Machine Learning`, aurai-je l'opportunité les mettre en oeuvre ?"
- "Nous avons énormément investi à constituer des jeux de données de qualité, des APIs efficaces et disponibles. Des travaux dans ce domaines sont en cours, toujours dans le but de faire plus, avec moins d'effort. Vous pourrez par exemple contribuer aux travaux que nous exposerons lors de #NODES24 cf https://x.com/rastadidi/status/1814417785952649288"


- "J'adore faire du `Go` : pourrai-je en faire ?"
- "Les logiciels que nous maintenons en interne sont sur la stack Java/Python. Toutefois, pour l'innovation externe, et à condition de respecter les règles du jeu, oui, cela est tout à fait possible, par exemple pour développer des produits clients de nos APIs publiques sur APIGEE, cf https://dev.to/adriens/mobitag-go-hackathon-2024-06-22-week-end-2n16". Cela peut également se traduire en innovations dans le cadre DevOPS



## 🥇 Comment se démarquer

Le procesus pour candidater est celui décrit sur l'AVP... toutefois, **si vous voulez faire la différence**,
vous pouvez venir avec un projet personnel à présenter et qui s'appuierait sur des APIs ou données publiées
par notre office telles que : 

- **Nos APIs publiques** sur notre marketplace d'APIs : https://rapidapi.com/organization/opt-nc 
- **Les jeux de données et notebooks** Jupyter publiés sur Kaggle : https://www.kaggle.com/optnouvellecaldonie
- **L'utilisation de nos images docker** pour réaliser un prototype innovant : https://hub.docker.com/u/optnc
- **La connaissance des nos articles** sur notre blog : https://dev.to/optnc
