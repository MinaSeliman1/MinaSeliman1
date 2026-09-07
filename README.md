# Mina Seliman

**Étudiant en Techniques de l'informatique — profil Génie logiciel**
Collège de Bois-de-Boulogne, Montréal · Basé à Laval, QC

> 🎯 **Je recherche un stage en développement logiciel pour la session d'hiver 2027.**
> Stage crédité de 8,66 unités — c'est l'épreuve synthèse de mon programme, à temps plein de janvier à mai 2027.

---

## 🔭 Ce sur quoi je travaille en ce moment

### [Vigie](https://github.com/MinaSeliman1/vigie) — conçu, développé et déployé seul

[![Démo](https://img.shields.io/badge/Démo-en%20ligne-17564A?style=flat-square)](https://minaseliman1.github.io/vigie/)
[![CI](https://github.com/MinaSeliman1/vigie/actions/workflows/ci.yml/badge.svg)](https://github.com/MinaSeliman1/vigie/actions/workflows/ci.yml)
[![Licence](https://img.shields.io/badge/licence-MIT-lightgrey?style=flat-square)](https://github.com/MinaSeliman1/vigie/blob/main/LICENSE)

Une application web de gestion de quarts pour équipes de sauveteurs — un métier que j'exerce moi-même à la Ville de Laval depuis 2023. Un collègue accepte un remplacement dans une conversation de groupe, le coordonnateur l'apprend après coup, et personne n'a vérifié si le remplaçant a les qualifications requises. Vigie centralise l'horaire, soumet les échanges à une approbation explicite et suit les certifications.

**Ce que le projet démontre :**

- **Architecture en quatre couches** — domaine, application, infrastructure, API — avec un domaine qui ne dépend d'aucune bibliothèque externe
- **47 endpoints REST** en ASP.NET Core (.NET 9) avec Entity Framework Core sur PostgreSQL, et 14 migrations
- **70 tests xUnit** : 32 tests de domaine qui s'exécutent sans base de données ni serveur, et 38 tests d'intégration — dont un qui verrouille le contrat OpenAPI de l'API
- **Cinq règles métier codifiées** : certifications, chevauchements, échanges approuvés, quotas horaires, saison d'ouverture
- **Sécurité et renseignements personnels** : authentification JWT par rôles, isolation des données entre organisations, mots de passe hachés en PBKDF2, limitation du débit, révocation des sessions, journal d'audit exportable, export et suppression des données d'un compte
- **Exploitation** : points de santé et de métriques, corrélation des requêtes, intégration continue GitHub Actions, API sur Render, PostgreSQL sur Supabase, interface React + TypeScript sur GitHub Pages

👉 **[Essayer la démo](https://minaseliman1.github.io/vigie/)** · **[Lire le code](https://github.com/MinaSeliman1/vigie)**

---

### [StockLab](https://github.com/MarcSaad-Hadidi/StockLab) — projet de session, équipe de trois

Une plateforme de simulation boursière multinuage, développée en approche agile.

Je suis **responsable du back-end** : conception et développement de l'API REST en **ASP.NET Core** avec **Entity Framework Core**, implémentation de la logique de portefeuille et du moteur de transactions, modélisation et exploitation de la base **Azure SQL**.

Je contribue aussi à l'architecture **multinuage** (Azure + AWS : Service Bus, Lambda, S3, SQS), à l'intégration de l'API boursière Twelve Data, et au raccordement d'un module d'apprentissage automatique en Python qui estime les tendances des titres.

---

## 🛠️ Stack

**Langages**
`C#` · `TypeScript` · `JavaScript` · `Java` · `SQL` · `HTML` · `CSS`

**Back-end et données**
`ASP.NET Core (.NET 9)` · `Entity Framework Core` · `API REST` · `PostgreSQL` · `Azure SQL` · `Node.js` · `Authentification JWT` · `Conception de schémas et migrations` · `Architecture en couches et n-tiers`

**Front-end**
`React` · `TypeScript` · `Vite` · `HTML/CSS` · `.NET MAUI` · `XAML`

**Qualité et déploiement**
`xUnit` · `Tests unitaires et d'intégration` · `GitHub Actions` · `Docker` · `Git` · `Render` · `Supabase` · `Postman` · `Visual Studio`

**Infonuagique**
`Microsoft Azure` · `AWS (S3, Lambda, SQS)` · `Linux` · `Windows`

**Méthodes**
`Agile` · `Modélisation UML` · `Intégration continue` · `MVVM` · `Injection de dépendances` · `Sécurité applicative`

---

## 📌 Projets

| Projet | Description | Stack |
|---|---|---|
| **[Vigie](https://github.com/MinaSeliman1/vigie)** — [démo](https://minaseliman1.github.io/vigie/) | Gestion de quarts pour équipes de sauveteurs : horaires, échanges approuvés, suivi des certifications. Conçu, développé et déployé seul — 47 endpoints, 70 tests, architecture en quatre couches, CI/CD. | ASP.NET Core · EF Core · PostgreSQL · React · TypeScript · xUnit · GitHub Actions · Render |
| **[StockLab](https://github.com/MarcSaad-Hadidi/StockLab)** | Plateforme de simulation boursière multinuage — portefeuille fictif, données de marché, transactions simulées. Projet d'équipe où je suis responsable du back-end et de l'architecture cloud. | ASP.NET Core · EF Core · Azure SQL · React · TypeScript · AWS · Python |
| **[Bibliothèque](https://github.com/MinaSeliman1/View)** | Application multiplateforme de gestion de bibliothèque (Android, iOS, macOS, Windows) — catalogue, favoris, évaluations, espace administrateur. Architecture MVVM en quatre projets avec tests unitaires. | .NET MAUI · C# · MVVM · XAML |

---

## 🎓 Formation

**DEC en Techniques de l'informatique, profil Génie logiciel** — Collège de Bois-de-Boulogne
*Août 2024 – mai 2027 (prévu)*

Cours pertinents : programmation objet 1 et 2, applications web transactionnelles, systèmes de bases de données, génie logiciel, sécurité des applications, architecture des réseaux, projet de développement de logiciel, applications mobiles.

**Certification** — Cisco Networking Academy, *CCNA : Présentation des réseaux* (août 2025)

---

## 🌍 Langues

Trilingue — **français**, **anglais**, **arabe égyptien**, à l'oral et à l'écrit.

---

## 📫 Me joindre

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mina--seliman-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mina-seliman-3b9184326)
[![Courriel](https://img.shields.io/badge/Courriel-minaseliman2007@hotmail.com-D14836?style=flat-square&logo=maildotru&logoColor=white)](mailto:minaseliman2007@hotmail.com)

Ouvert aux stages en développement back-end, full-stack ou infonuagique dans la région de Montréal et Laval.
