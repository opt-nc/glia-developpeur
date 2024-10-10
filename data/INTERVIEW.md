## ❔ A propos

Le but de ce document est de fournir un ensemble de questions/réponses permettant
de **mieux cerner les spécificités du poste de Développeur au GLIA.**

## 🧑‍🤝‍🧑 Organsiation du travail et collaboration

Ci-dessous un exemple de Questions (Q)/ Réponses (R):

- Q: "Est-t-il possible de travailler à distance ?"
- R: "Oui, à hauteur de 2 jours maximum par semaine et sur des créneaux horaires convenus à l'avance, à l'exceptiondu jeudi après-midi où la présence est sur site est exigée."


- Q: "Pourquoi le jeudi après-midi est-il obligatoire ?"
- R: "Ce créneau est réservé à l'unique SCRUM hebdomadaire, et aux échanges informels entre les membres de l'équipe ainsi qu'aux sujets d'innovation."

- Q: "Utilisez-vous SCRUM pour organiser le travail du bureau?"
- R: "Non, nous sommes sur la méthode Kanban, plus adaptée à la nature et la variété des missions du bureau."

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
3. **Installer la dernière Ubuntu `LTS` en cours (voir les détails : https://endoflife.date/ubuntu)
4. **Prendre en charge un projet d'innovation** qui vous sera proposé et que vous devrez mener à bien de bout en bout, dans le respect des méthodes et outils de l'équipe: ce projet sera votre fil rouge pour votre intégration
5. **Participer** au premier SCRUM et présenter vos avancées


## 🧰 La stack technique

Ci-dessous un exemple de Questions (Q)/ Réponses (R):

- Q: "Quelle distribution Linux utilisez-vous ?"
- R: "**L'unique distriution Linux supportée au GLIA est Ubuntu, et systématiquement dans sa dernière version LTS**. Il est également exigé de chiffrer l'intégralité du filesystem (Full disk encryption) et d'activer Ubuntu Pro."

- Q: "Je suis fan de Pop!_OS et Linux Mint, c'est OK donc si je l'utilise au bureau ?"
- R: "NON : l'unique distriution Linux supportée au GLIA est Ubuntu : : il est expressément demander de respecter cela. Si vous avez un environnement bureau préféré, alors il vous reviendra de le configruer."

- Q: "Je suis fan de Arch : c'est OK donc si je l'utilise au bureau ?"
- R: "NON : l'unique distriution Linux supportée au GLIA est Ubuntu : il est expressément demander de respecter cela."

- Q: "Je veux pas utiliser Ubuntu : c'est OK si j'utiliser une autre distribution au bureau ?"
- R: "NON : l'unique distriution Linux supportée au GLIA est Ubuntu : il est expressément demander de respecter cela."
 

- Q: "Quelle est la stack Java utilisée ?"
- R: "Nous utilions Maven pour builder, Quarkus pour les microservices et batches, et maintenons des applications Spring Boot historiques... en cours de migration vers Quarkus."


- Q: "Quelle votre base de données relationnelle pour les développements spécifiques?"
- R: "Nous utilisons PostgreSQL pour les développements spécifiques."


- Q: "Quels sont les outils que je vais devoir installer sur ma workstation?"
- R: "Tous les outils de build, principalement Maven, Podman et Git, ainsi que les outils de développement Java, IntelliJ IDEA ou VSCode selon vos préférences."


- Q: "Utilisez-vous des containers ?"
- R: "Oui, systématiquement, pour tout, partout et tout le temps. Nous utilisons Podman pour les containers, et Ansible/Tower pour les déploiements via des GtiHub actions déidées. Tout est systématiquement livré sous forme de containers, en continu via la registry ghcr.io de Github.com. Les tests sont également déroulées via Testcontainers (https://testcontainers.com/)."


- Q: "Comment exécutez-vous les containers ?"
- R: "DEVs et OPs partagent la même stack technique (de bout en bout), et les containers sont exécutés en local via Podman, et en production via Podman pour l'instant. Tout est automatisé via Ansible/Tower."


- Q: "Quels sont les middleware utilisés ?"
- R: "Le GLIA utilise Kafka (développement de producers, consumers, streams,...) pour les échanges asynchrones, et la haute disponibilité, Open Search pour les recherches full text et les logs, PostgreSQL pour les bases de données relationnelles, consul pour partager des configurations, Neo4J pour la cartographie du SI."


- Q: "Avec quoi buildez-vous vos applications ?"
- R: "On builde avec Maven, et on teste avec JUnit, TestContainers (et d'autres frameworks cloud-natifs encore en cours d'intégration) via des actions Github et des workflows dédiés"


- Q: "Où sont gérées les issues ?"
- R: "Les issues de support arrivent via un système de ticket externe que nous avons intégré à Github, et les issues de développement sont gérées via Github. Elles sont totalement liées au processus de build, de déploiement et de maintenance des applications."


- Q: "Quelle CI utilisez-vous ?"
- R: "Nous utilisons tous les services mis à disposition par Github, et en particulier les actions Github pour les workflows de build, de test, de déploiement, et de maintenance."


- Q: "Commment délivrez-vous vos applications ?"
- R: "Nous délivrons nos images sur ghcr.io, l'automatication est faite via Ansible/Tower qui vient puller et démarrer les containers sur les serveurs d'intégration, qualification et production. Voir https://github.com/opt-nc/tower-deploy-action"


- Q: "Comment documentez-vous vos APIs ?"
- R: "Nous développons nos APIs avec Quarkus, nous générons la documentation en continu , notamment avec redocly, cf https://dev.to/optnc/api-documentation-release-automation-with-github-redocly-and-open-api-f6h"


- Q: "Utilisez-vous Kafka ?"
- R: "Oui, en permanence, Kafka est au coeur de l'ADN du bureau, pour les échanges asynchrones, la haute disponibilité, la scalabilité et l'interopérabilité."


- Q: "Faites-vous de la data science ?"
- R: "Oui, nous mettons un point d'honneur à décrire les choses avec des données, des APIs,...puis de les valoriser via des applications, des dashboards, des rapports, des analyses, des prédictions, des recommandations, des alertes,... Nous faisons cela avec du Python."


- Q: "Utilisez-vous des bases de données NoSQL ?"
- R: "Oui, à ce jour de l'OpenSearch et sdu Neo4J."


- Q: "Utilisez-vous du Python ?... et si oui, pour quoi faire ?"
- R: "Oui, pour la datascience, les analyses, des automatisations ou au sein de la CI/CD pour automatiser des traitements, des tests, des déploiements."


- Q: "Sécurisez-vous vos artefacts/images docker... et si oui, comment ?"
- R: "La sécurité et la dette technique sont au coeur de nos préoccupations. Nous utilisons dependabot pour nous aider et `grype` pour choisir les images de base sur lesquelles nous nous appuyons par la suite. Par exemple, notre choix pour Kafka https://dev.to/optnc/kafka-image-wurstmeister-vs-bitnami-efg ou encore celui de Java : https://dev.to/optnc/bench-and-choose-java-8-docker-images-with-anchoregrype-4fg8

-  Q: "Je fais du Kubernetes : en faites-vous ?"
-  R: "Kubernetes est entrain de rentrer sur notre stack, **mais pour l'instant pas pour faire de la production**. Nous avons fait le choix de Google Anthos. Nous avons préparé quelques HELM charts et déployé des applications en mode développement via Argo CD. Notre priorité est actuellement de finaliser le tournant vers la conteneurisation et l'automatisation qui va avec. Toutefois, oui, vous pourrez mettre à profit (et développer) vos compétences pour par exemple déployer des applications sur notre environnement de développement, en partageant et en répondant à des problématiques du bureau. Sur les postes de développeurs, nous privilégions MicroK8s. Et pour tester en mode innovation publique nous utilisons la plateforme Killercoda, pour cela regarder la page de notre organisation : https://killercoda.com/opt-labs/"

-  Q: "J'aime me former en continu : quelles sont les opportunités dans ce domaine?"
-  R: "Pour se former, l'innovation est au coeur de nos activités. En plus de cela, nous bénéficions de faciliter par exemple via Google Cloud Skills Boost. Les formations sont toujours effectuées juste avant une mise en pratique et sont donc liées aux problématiques remontées depuis le terrain, les collaborateurs, les incidents éventuels ou les projets."

- Q: "Je suis très bon en Kotlin, node, Flutter, Vuejs, Nextjs : est-ce que je peux décider de développer dessus ?"
- R: "Le processus d'adoption de nouvelles briques sur notre chaîne de BUILD et **pipeline DevOPS est une partie extrêmement sensible** car elle impacte notre productivité et notre capacité à rendre durablement... à un coût minimal mais pour délivrer un service optimal. Donc non, on ne décide pas comme cela de choisir une nouvelle techno "cool", en revanche les problématiques de productivité, de sécurité et de durabilité de la maintenance du SI sont regardées avec un très grand soin et au final tranchées par le responsable du bureau puisqu'au final ce sera l'ensemble de l'équipe qui sera impactée au quotidien. Lors de nouveaux choix, on teste sur des périmètres très restreints et avec un sens aigu du partage des avancées et du feedback."

-  Q: "J'utilise une autre distribution qu'Ubuntu : je peux utiliser Fedora ou Arch ?"
-  R: "Non, Ubuntu est la distribution de base que nous avons choisie ensemble entre DEVs et OPS. Nous avons mis des efforts importants pour documenter certaines configurations complexes à mettre en oeuvre afin de limiter les efforts collectifs."

## 🔍 La stack de test logiciel

Le test logiciel occupe une place très importante au bureau puisque c'est grâce à elle que nous pouvons délivrer très rapidement et en continu des évolutions ou dérouler notre processus de maintenance. En C'est la stack de test qui nous permet de faire cela et ainsi réduire le "Time to Market".
En particulier, **nous faisons notre maximum pour éradiquer les tests en `e2e` au profit de tests d'intégration continue** et conteneurisés sur la partie dont nous avons la charge.

Pour les TUs (tests unitaires), nous utilisons
- Junit,
- jacoco (https://www.eclemma.org/jacoco) pour mesurer le taux de couverture,
- Les testcontainers, docker et images natives,
- Les matrices (https://docs.github.com/en/actions/writing-workflows/choosing-what-your-workflow-does/using-a-matrix-for-your-jobs#using-a-matrix-strategy) sur Github afin de tester différentes versions d'OS, de Java ou de bases de données,...,
- Tests via Embeddedkafka (en cours de migration vers autre technologie),
- Tests à venir via Microcks (https://microcks.io/)

## 🧑‍🚀 Culture de l'innovation

Ci-dessous un exemple de Questions (Q)/ Réponses (R):

- Q: "J'ai cru comprendre que l'innovation était une valeur forte de l'équipe, comment cela se traduit-il ?"
- R: "Oui, tout à fait et nous la mettons en oeuvre au quotidien.  Nous sommes adeptes du _"Eating your own dog food"_. Nous mettons un point d'honneur à innover pour pouvoir répondre à des problématiques du quotidien pour nous ou nos clients. Les sujets sont décidés au sein de l'équipe et sont souvent issus de difficultés rencontrées lors du BUILD ou RUN. Les résultats sont systématiquement documentés, démontrés et s'ils ne devaient mener à rien, alors c'est dans un mode de "fail fast" que nous les abandonnons. Le critère de mise à l'échelle de l'innovation est central pour nous."


- Q: "J'ai des compétences en `Machine Learning`, aurai-je l'opportunité les mettre en oeuvre ?"
- R: "Nous avons énormément investi à constituer des jeux de données de qualité, des APIs efficaces et disponibles. Des travaux dans ce domaines sont en cours, toujours dans le but de faire plus, avec moins d'effort. Vous pourrez par exemple contribuer aux travaux que nous exposerons lors de #NODES24 cf https://x.com/rastadidi/status/1814417785952649288"


- Q: "J'adore faire du `Go` : pourrai-je en faire ?"
- R: "Les logiciels que nous maintenons en interne sont sur la stack Java/Python. Toutefois, pour l'innovation externe, et à condition de respecter les règles du jeu, oui, cela est tout à fait possible, par exemple pour développer des produits clients de nos APIs publiques sur APIGEE, cf https://dev.to/adriens/mobitag-go-hackathon-2024-06-22-week-end-2n16". Cela peut également se traduire en innovations dans le cadre DevOPS

- Q: "Je fais de l'IoT : est-t-il possible d'en faire ?"
- R: "La vocation du bureau n'est pas de faire de l'IoT. En revanche, il peut être possible d'organiser des intégrations dans la mesure où elles permettent d'optimiser la productivité des collaborateurs, de mettre en valeur une API, une technologie. Ci-après quelques exemples de réalisations autour de système de notification de courrier ou de boîtes postales se reposant sur des services en cloud : https://www.hackster.io/354529/mailbox-notifier-ed6dba, https://www.hackster.io/adriensales/legacy-mailbox-sms-notifier-ec6d4b. Du matériel perso peut être mis à disposition mais le cadrage de ces prototypes doit être cadré de manière drastique, toujours dans la philosphie LEAN. Généralement on fait cela dans un cadre de Team Building. On peut utiliser de l'Arduino, du Seeed, les matrices de LED, du eInk,... et bien sûr les APIs publiques de l'OPT ;-p"

- Q: "Je programme des jeux/moteurs 3d sur mon temps libre (Unity/Blender) : je pourrais mettre mes compétences au service du bureau ?"
- R: "Cela ne fait en effet pas partie de la stack du bureau. En revanche, pour du dataviz, cela pourrait être utilisé, par exemple pour mettre en évidence le potentiel de certaines données ou APIs. Par exemple, les réalisation de data-art réalisées sur les temps d'attente en agence : https://dev.to/adriens/series/18414"

- Q: "Je vois que vous avez écrit des articles : devrai-je en écrire, aurai-je l'opportunité d'en écrire moi-même ?"
- R: "En effet, nous postons des articles à porté publique sur https://dev.to/optnc. Oui, je vous demanderai d'en écrire, dans le but de développer le sens de la synthèse, de partager efficacement et durablement les connaissances acquises et qui seront par la suite mises en oeuvre à l'échelle, par exemple https://dev.to/optnc/api-marketplaces-innovation-explained-and-showcased-li1, https://dev.to/optnc/effortless-data-quality-wduckdb-on-github-2mkb, https://dev.to/optnc/ridet-nc-api-service-mesh-api-on-top-of-heterogeneous-open-data-4c3b, https://dev.to/optnc/follow-delivery-in-new-caledonia-with-rapidapi-4bh9, https://dev.to/optnc/sending-flat-files-to-kafka-2n06, https://dev.to/optnc/get-started-with-apigee-management-55dg, https://dev.to/optnc/better-collab-flows-w-git-conventional-commits-49j8. La production d'un article est le fruit d'un processus complet qui nous permet de progresser à plusieurs... et avec un standard de qualité que j'aime à qualifier d'international puisque applicable partout, y compris hors du contexte de l'office."

## 🥇 Comment se démarquer

Le procesus pour candidater au bureau (pour un AVP ou un stage par exemple) est très normé... toutefois, **si vous voulez faire la différence**,
vous pouvez venir avec un projet personnel à présenter et qui s'appuierait sur des APIs ou données publiées
par notre office telles que : 

- **Nos APIs publiques** sur notre marketplace d'APIs : https://rapidapi.com/organization/opt-nc 
- **Les jeux de données et notebooks** Jupyter publiés sur Kaggle : https://www.kaggle.com/optnouvellecaldonie
- **L'utilisation de nos images docker** pour réaliser un prototype innovant : https://hub.docker.com/u/optnc
- **La connaissance des nos articles** sur notre blog : https://dev.to/optnc

## 💼  Recrutement

- Q: "Recrutez-vous actuellement?"
- A: "Non, il n'y a pas d'AVP en cours pour le GLIA, je vous encourage à aller voir les AVPs et offres d'emplois : https://office.opt.nc/fr/emploi-et-carriere/rejoindre-l-opt-nc#avp-et-offres-d-emploi"

- Q: "J'aimerai faire un stage: est-ce possible?"
- A: "Pour cela il faut candidater. La préparation d'un dossier détaillant motivation et compétences est un prérequis"
