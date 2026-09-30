# Mina Seliman

**Étudiant en Techniques de l'informatique — profil Génie logiciel**
Collège de Bois-de-Boulogne, Montréal · Basé à Laval, QC

> 🎯 **Je recherche un stage en génie logiciel pour la session d'hiver 2027.**
> Stage crédité de 8,66 unités — c'est l'épreuve synthèse de mon programme, à temps plein de janvier à avril 2027.

`C#` `.NET 9` `ASP.NET Core` `Entity Framework Core` `Go` `Python` `TypeScript` `JavaScript` `Java` `SQL` `React` `Vue 3` `Node.js` `REST` `GraphQL` `PostgreSQL` `TimescaleDB` `Azure SQL` `Kafka` `Docker` `Kubernetes` `Helm` `GitHub Actions` `Azure` `AWS` `xUnit` `pytest` `Vitest` `Playwright` `Prometheus` `Git`

---

## 🔭 Ce sur quoi je travaille en ce moment

### [Vigie](https://github.com/MinaSeliman1/vigie) — conçu, développé et déployé seul

[![Démo](https://img.shields.io/badge/Démo-en%20ligne-17564A?style=flat-square)](https://minaseliman1.github.io/vigie/)
[![CI](https://github.com/MinaSeliman1/vigie/actions/workflows/ci.yml/badge.svg)](https://github.com/MinaSeliman1/vigie/actions/workflows/ci.yml)
[![Licence](https://img.shields.io/badge/licence-MIT-lightgrey?style=flat-square)](https://github.com/MinaSeliman1/vigie/blob/main/LICENSE)

Une application web de gestion de quarts pour équipes de sauveteurs — un métier que j'exerce moi-même à la Ville de Laval depuis 2023. Un collègue accepte un remplacement dans une conversation de groupe, le coordonnateur l'apprend après coup, et personne n'a vérifié si le remplaçant a les qualifications requises. Vigie centralise l'horaire, soumet les échanges à une approbation explicite et suit les certifications.

**Stack et outils**
`C#` `.NET 9` `ASP.NET Core` `Minimal APIs` `Entity Framework Core 9` `Npgsql` `PostgreSQL` `LINQ` `Migrations EF` `API REST` `OpenAPI / Swagger` `JWT Bearer` `Authentification par rôles` `PBKDF2` `Rate limiting` `Multi-tenant` `Journal d'audit` `Protection des renseignements personnels` `Architecture en couches` `Domain-Driven Design` `Injection de dépendances` `Nullable reference types` `TreatWarningsAsErrors` `React 19` `TypeScript` `Vite` `Vitest` `oxlint` `HTML5` `CSS3` `Responsive design` `Fetch API` `SPA` `xUnit` `Tests d'intégration` `Tests de contrat OpenAPI` `Docker` `Docker Compose` `GitHub Actions` `CI/CD` `Render` `Supabase` `GitHub Pages` `Health checks` `Métriques` `Corrélation de requêtes` `Git` `GitHub` `Markdown`

**Ce que le projet démontre :**

- **Architecture en quatre couches** — domaine, application, infrastructure, API — avec un domaine qui ne dépend d'aucune bibliothèque externe
- **47 endpoints REST** en ASP.NET Core (.NET 9) avec Entity Framework Core sur PostgreSQL, et 14 migrations
- **70 tests xUnit** : 32 tests de domaine qui s'exécutent sans base de données ni serveur, et 38 tests d'intégration — dont un qui verrouille le contrat OpenAPI de l'API
- **Cinq règles métier codifiées** : certifications, chevauchements, échanges approuvés, quotas horaires, saison d'ouverture
- **Sécurité et renseignements personnels** : authentification JWT par rôles, isolation des données entre organisations, mots de passe hachés en PBKDF2, limitation du débit, révocation des sessions, journal d'audit exportable, export et suppression des données d'un compte
- **Exploitation** : points de santé et de métriques, corrélation des requêtes, intégration continue GitHub Actions, API sur Render, PostgreSQL sur Supabase, interface React + TypeScript sur GitHub Pages

👉 **[Essayer la démo](https://minaseliman1.github.io/vigie/)** · **[Lire le code](https://github.com/MinaSeliman1/vigie)**

---

### [Ponctuel](https://github.com/MinaSeliman1/Ponctuel) — plateforme temps réel, architecture microservices

Une plateforme qui mesure la ponctualité réelle du transport en commun montréalais : elle décode le flux temps réel de la STM, en déduit les heures d'arrivée réellement observées, et les compare aux prédictions annoncées aux usagers. Cinq services indépendants, du protobuf jusqu'au tableau de bord.

**Stack et outils**
`Go 1.27` `Microservices` `Architecture événementielle` `Redpanda` `Apache Kafka (API)` `kafka-go` `Protocol Buffers` `GTFS-Realtime` `GTFS` `pgx` `TimescaleDB` `PostgreSQL 17` `Séries temporelles` `SQL` `gqlgen` `GraphQL` `Schéma GraphQL` `Python 3.12` `FastAPI` `Uvicorn` `Pydantic` `scikit-learn` `NumPy` `joblib` `httpx` `Vue 3` `TypeScript` `Vite` `vue-tsc` `Vitest` `Vue Test Utils` `jsdom` `Playwright` `Tests E2E` `Docker` `Dockerfile multi-étapes` `Docker Compose` `Kubernetes` `Helm` `helm lint` `k3s` `Oracle Cloud (OCI)` `Render` `GitHub Actions` `CI/CD` `gitleaks` `Analyse de secrets` `go vet` `pytest` `Prometheus` `Observabilité` `Git`

**Ce que le projet démontre :**

- **Chaîne événementielle complète** — un *ingester* en Go décode le flux GTFS-Realtime (Protocol Buffers) de la STM et le publie dans **Redpanda** (compatible API Kafka) ; un *matcher* en consomme les événements ; une API GraphQL les expose ; un tableau de bord Vue 3 les affiche
- **Deux méthodes d'inférence implémentées indépendamment puis comparées** pour déduire l'arrivée réelle d'un véhicule — parce qu'une mesure sans contre-mesure n'est pas une mesure
- **Stockage en série temporelle** dans TimescaleDB, avec des agrégats qui conservent toujours leur nombre d'observations : l'interface ne montre jamais une statistique qu'elle ne peut pas défendre
- **Service de prédiction en Python** (FastAPI + scikit-learn) branché sur la même chaîne
- **Chaîne d'intégration continue en 8 jobs** : tests Go, tests d'intégration sur une vraie base TimescaleDB, tests et *typecheck* front-end, tests navigateur Playwright, tests Python, construction des cinq images Docker, analyse de secrets gitleaks, et validation du chart Helm
- **Déployable de trois façons** : Docker Compose, chart Helm sur Kubernetes, ou Oracle Cloud

👉 **[Lire le code](https://github.com/MinaSeliman1/Ponctuel)**

---

### [Trading Bot Research](https://github.com/MinaSeliman1/trading-bot) — quatre stratégies testées, quatre rejetées

[![Python](https://img.shields.io/badge/Python-pandas%20·%20NumPy%20·%20scikit--learn-3776AB?style=flat-square)](https://github.com/MinaSeliman1/trading-bot)
[![Résultat](https://img.shields.io/badge/résultat-négatif%20et%20assumé-7A3E3E?style=flat-square)](https://github.com/MinaSeliman1/trading-bot/blob/master/lessons_learned.md)

Un projet de recherche quantitative en Python. Quatre stratégies indépendantes — retour à la moyenne et suivi de tendance, dérive post-annonce de résultats (PEAD), fade de l'*opening range* en intrajournalier, vente d'options de vente mensuelles — soumises à la même discipline de validation. **Aucune n'a passé la barre, et le dépôt le dit en première ligne.** `bot/main.py` refuse de démarrer : rien ne négocie d'argent réel.

**Stack et outils**
`Python` `pandas` `NumPy` `SciPy` `scikit-learn` `Matplotlib` `pyarrow` `Parquet` `yfinance` `alpaca-py` `alpaca-trade-api` `python-dotenv` `pytest` `Analyse de données` `Séries temporelles` `Statistiques` `Validation walk-forward` `Tests hors échantillon` `Analyse multi-régimes` `Backtesting` `Gestion du risque` `SEC EDGAR` `XBRL` `Alpha Vantage` `API REST` `Mise en cache` `ETL` `Ingénierie de caractéristiques` `Reproductibilité`

**Pourquoi publier un projet qui « n'a pas marché » :** un résultat négatif obtenu rigoureusement est un résultat. Ce que le dépôt démontre, ce n'est pas une stratégie gagnante — c'est la méthode.

- **Validation *walk-forward* et multi-régimes** — une stratégie qui règle un problème pendant le marché baissier lent de 2021-2022 peut le détruire pendant la correction rapide du T4 2018. Tester sur un seul régime ne prouve rien.
- **Mesure d'un piège classique** : sur PEAD, le paramètre optimal en échantillon se classait *moins bien qu'un tirage au hasard* hors échantillon.
- **Un ratio de Sharpe de 8+ a été enquêté, pas publié** — c'était un bogue d'interpolation linéaire dans la valorisation, qui gonflait le résultat de 10 à 50 fois.
- **Limites des sources de données vérifiées en direct, jamais supposées** : un flux IEX plus court que documenté, une correspondance ticker → CIK erronée dans les données de référence de la SEC elle-même, et un défaut de yfinance qui renvoie silencieusement des prix ajustés plutôt que les prix réellement négociés.
- **Pipeline de données** : fondamentaux trimestriels XBRL de SEC EDGAR, barres de prix et chaînes d'options Alpaca, historique de surprises de résultats Alpha Vantage, avec mise en cache pour ne jamais redépenser un quota.

👉 **[La méthodologie (`lessons_learned.md`)](https://github.com/MinaSeliman1/trading-bot/blob/master/lessons_learned.md)** — le fichier le plus réutilisé du dépôt

---

### [StockLab](https://github.com/MarcSaad-Hadidi/StockLab) — projet de session, équipe de trois

Une plateforme de simulation boursière multinuage, développée en approche agile.

**Stack et outils**
`C#` `ASP.NET Core` `Entity Framework Core` `API REST` `Azure SQL` `Microsoft Azure` `Azure Service Bus` `AWS` `AWS Lambda` `Amazon S3` `Amazon SQS` `Architecture multinuage` `Messagerie asynchrone` `Serverless` `React` `TypeScript` `Python` `scikit-learn` `Twelve Data API` `Intégration d'API tierces` `Agile` `Scrum` `Sprints` `Revue de code` `Git` `GitHub` `Travail en équipe`

Je suis **responsable du back-end** : conception et développement de l'API REST en **ASP.NET Core** avec **Entity Framework Core**, implémentation de la logique de portefeuille et du moteur de transactions, modélisation et exploitation de la base **Azure SQL**.

Je contribue aussi à l'architecture **multinuage** (Azure + AWS : Service Bus, Lambda, S3, SQS), à l'intégration de l'API boursière Twelve Data, et au raccordement d'un module d'apprentissage automatique en Python qui estime les tendances des titres.

---

### [Bibliothèque](https://github.com/MinaSeliman1/View) — application multiplateforme .NET MAUI

Gestion de bibliothèque déployée sur Android, iOS, macOS et Windows à partir d'une base de code unique. Les lecteurs consultent un catalogue, tiennent une liste de favoris et évaluent les livres ; les administrateurs gèrent le catalogue et les comptes depuis un tableau de bord distinct, avec authentification par rôles et session persistante.

**Stack et outils**
`C#` `.NET 9` `.NET MAUI` `XAML` `MVVM` `AppShell` `INotifyPropertyChanged` `Data binding` `Injection de dépendances` `Programmation par interfaces` `Sérialisation XML` `Tests unitaires` `Architecture en couches` `Android` `iOS` `macOS (Mac Catalyst)` `Windows` `Multiplateforme` `Développement mobile`

**Ce que le projet démontre :**

- **Quatre projets plutôt qu'un monolithe** — `Bibliotheque.Model` (entités du domaine, sans aucune dépendance), `Bibliotheque.Services` (logique métier), `Bibliotheque.ViewModel` (MVVM), `View` (interface .NET MAUI en XAML) — plus un projet de tests unitaires
- **MVVM strict** : aucune logique métier dans le code-behind des pages XAML, ce qui rend la couche métier testable sans jamais lancer l'interface
- **Services derrière des interfaces** (`IAuthService`, `IBibliothequeXmlService`, `IFavorisService`), injectés depuis `MauiProgram.cs` — remplacer la persistance par une base de données ne demanderait que d'écrire une nouvelle implémentation, sans toucher au reste de l'application
- **Persistance par sérialisation XML** — un choix assumé pour un projet scolaire : aucun serveur, aucune dépendance externe
- **Cibles** : Android 21+, iOS 15+, Mac Catalyst 15+, Windows 10 17763+

---

## 🛠️ Stack complète

**Langages**
`C#` · `Go` · `Python` · `TypeScript` · `JavaScript` · `Java` · `SQL` · `HTML5` · `CSS3` · `Bash` · `YAML` · `Markdown` · `GraphQL (SDL)` · `Protocol Buffers`

**Back-end**
`ASP.NET Core (.NET 9)` · `Minimal APIs` · `Entity Framework Core` · `Node.js` · `FastAPI` · `Uvicorn` · `Pydantic` · `gqlgen` · `API REST` · `GraphQL` · `OpenAPI / Swagger` · `Architecture microservices` · `Architecture événementielle` · `Architecture en couches et n-tiers` · `Domain-Driven Design` · `Injection de dépendances` · `Programmation asynchrone` · `Conception d'API`

**Front-end**
`React 19` · `Vue 3` · `TypeScript` · `JavaScript` · `Vite` · `HTML5` · `CSS3` · `Responsive design` · `SPA` · `Fetch API` · `.NET MAUI` · `XAML` · `MVVM`

**Bases de données**
`PostgreSQL` · `TimescaleDB` · `Azure SQL` · `SQL Server` · `SQL` · `LINQ` · `Npgsql` · `pgx` · `Conception de schémas` · `Migrations` · `Indexation` · `Séries temporelles` · `Modélisation de données`

**Données et analyse**
`pandas` · `NumPy` · `SciPy` · `scikit-learn` · `Matplotlib` · `pyarrow` · `Parquet` · `joblib` · `API SEC EDGAR (XBRL)` · `Validation walk-forward` · `Backtesting` · `ETL` · `Apprentissage automatique`

**Messagerie et temps réel**
`Apache Kafka (API)` · `Redpanda` · `kafka-go` · `Azure Service Bus` · `Amazon SQS` · `Publication/abonnement` · `Protocol Buffers` · `GTFS-Realtime` · `Traitement de flux`

**Qualité et tests**
`xUnit` · `pytest` · `Vitest` · `Vue Test Utils` · `Playwright` · `Tests unitaires` · `Tests d'intégration` · `Tests de bout en bout` · `Tests de contrat d'API` · `go vet` · `oxlint` · `Revue de code` · `TreatWarningsAsErrors` · `Débogage` · `Postman`

**DevOps et infonuagique**
`Git` · `GitHub` · `GitHub Actions` · `CI/CD` · `Docker` · `Docker Compose` · `Kubernetes` · `Helm` · `k3s` · `Linux` · `Windows` · `Microsoft Azure` · `AWS (Lambda, S3, SQS)` · `Oracle Cloud (OCI)` · `Render` · `Supabase` · `GitHub Pages` · `Prometheus` · `Observabilité` · `Health checks` · `Analyse de secrets (gitleaks)`

**Sécurité**
`Authentification JWT` · `Contrôle d'accès par rôles` · `PBKDF2` · `Hachage de mots de passe` · `Limitation de débit` · `Isolation multi-tenant` · `Journal d'audit` · `Gestion des secrets` · `Sécurité applicative` · `Protection des renseignements personnels`

**Méthodes et outils**
`Agile` · `Scrum` · `Modélisation UML` · `Conception orientée objet` · `Patrons de conception` · `Structures de données et algorithmes` · `Visual Studio` · `Visual Studio Code` · `Documentation technique`

**Réseaux**
`TCP/IP` · `HTTP/HTTPS` · `DNS` · `Cisco CCNA (Introduction aux réseaux)` · `Routage et commutation` · `Modèle OSI`

---

## 📌 Vue d'ensemble des projets

| Projet | Description | Stack |
|---|---|---|
| **[Vigie](https://github.com/MinaSeliman1/vigie)** — [démo en ligne](https://minaseliman1.github.io/vigie/) | Gestion de quarts pour équipes de sauveteurs : horaires, échanges approuvés, suivi des certifications. Conçu, développé et déployé seul — 47 endpoints, 70 tests, architecture en quatre couches, CI/CD. | C# · ASP.NET Core · .NET 9 · EF Core · PostgreSQL · React 19 · TypeScript · Vite · JWT · OpenAPI · xUnit · Vitest · Docker · GitHub Actions · Render · Supabase · GitHub Pages |
| **[Ponctuel](https://github.com/MinaSeliman1/Ponctuel)** | Plateforme temps réel qui mesure la ponctualité du transport en commun : cinq microservices, du flux protobuf de la STM jusqu'au tableau de bord. | Go · Redpanda (Kafka) · Protocol Buffers · GTFS-Realtime · TimescaleDB · pgx · GraphQL (gqlgen) · Vue 3 · TypeScript · Python · FastAPI · scikit-learn · Playwright · Docker · Kubernetes · Helm · Oracle Cloud · Prometheus · gitleaks |
| **[Trading Bot Research](https://github.com/MinaSeliman1/trading-bot)** | Recherche quantitative : quatre stratégies testées en validation walk-forward et multi-régimes, quatre rejetées. Le livrable est la méthodologie, pas une stratégie. | Python · pandas · NumPy · SciPy · scikit-learn · Matplotlib · pyarrow · pytest · SEC EDGAR (XBRL) · Alpaca · yfinance · backtesting |
| **[StockLab](https://github.com/MarcSaad-Hadidi/StockLab)** | Plateforme de simulation boursière multinuage — portefeuille fictif, données de marché, transactions simulées. Projet d'équipe où je suis responsable du back-end et de l'architecture cloud. | C# · ASP.NET Core · EF Core · Azure SQL · Azure Service Bus · AWS Lambda · S3 · SQS · React · TypeScript · Python · Agile |
| **[Bibliothèque](https://github.com/MinaSeliman1/View)** | Application multiplateforme de gestion de bibliothèque (Android, iOS, macOS, Windows) — catalogue, favoris, évaluations, espace administrateur. Quatre projets, MVVM strict, services derrière des interfaces, tests unitaires. | C# · .NET 9 · .NET MAUI · XAML · MVVM · injection de dépendances · sérialisation XML · tests unitaires |

---

## 🎓 Formation

**DEC en Techniques de l'informatique, profil Génie logiciel** — Collège de Bois-de-Boulogne
*Août 2024 – mai 2027 (prévu)*

Cours pertinents : programmation objet 1 et 2, structures de données et algorithmes, applications web transactionnelles, systèmes de bases de données, génie logiciel, sécurité des applications, architecture des réseaux, projet de développement de logiciel, applications mobiles.

**Certification** — Cisco Networking Academy, *CCNA : Présentation des réseaux* (août 2025)

---

## 🌍 Langues

Trilingue — **français**, **anglais**, **arabe égyptien**, à l'oral et à l'écrit.

---

## 📫 Me joindre

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mina--seliman-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mina-seliman-3b9184326)
[![Courriel](https://img.shields.io/badge/Courriel-minaseliman2007@hotmail.com-D14836?style=flat-square&logo=maildotru&logoColor=white)](mailto:minaseliman2007@hotmail.com)

Ouvert aux stages en développement logiciel, web, back-end, données ou infonuagique dans la région de Montréal et Laval.
