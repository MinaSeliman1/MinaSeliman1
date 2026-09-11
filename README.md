# Mina Seliman

**Étudiant en Techniques de l'informatique — profil Génie logiciel**
Collège de Bois-de-Boulogne, Montréal · Basé à Laval, QC

> 🎯 **Je recherche un stage en génie logiciel pour la session d'hiver 2027.**
> Stage crédité de 8,66 unités — c'est l'épreuve synthèse de mon programme, à temps plein de janvier à avril 2027.

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

### [Trading Bot Research](https://github.com/MinaSeliman1/trading-bot) — quatre stratégies testées, quatre rejetées

[![Python](https://img.shields.io/badge/Python-pandas%20·%20NumPy%20·%20scikit--learn-3776AB?style=flat-square)](https://github.com/MinaSeliman1/trading-bot)
[![Résultat](https://img.shields.io/badge/résultat-négatif%20et%20assumé-7A3E3E?style=flat-square)](https://github.com/MinaSeliman1/trading-bot/blob/master/lessons_learned.md)

Un projet de recherche quantitative en Python. Quatre stratégies indépendantes — retour à la moyenne et suivi de tendance, dérive post-annonce de résultats (PEAD), fade de l'*opening range* en intrajournalier, vente d'options de vente mensuelles — soumises à la même discipline de validation. **Aucune n'a passé la barre, et le dépôt le dit en première ligne.** `bot/main.py` refuse de démarrer : rien ne négocie d'argent réel.

**Pourquoi publier un projet qui « n'a pas marché » :** un résultat négatif obtenu rigoureusement est un résultat. Ce que le dépôt démontre, ce n'est pas une stratégie gagnante — c'est la méthode.

- **Validation *walk-forward* et multi-régimes** — une stratégie qui règle un problème pendant le marché baissier lent de 2021-2022 peut le détruire pendant la correction rapide du T4 2018. Tester sur un seul régime ne prouve rien.
- **Mesure d'un piège classique** : sur PEAD, le paramètre optimal en échantillon se classait *moins bien qu'un tirage au hasard* hors échantillon.
- **Un ratio de Sharpe de 8+ a été enquêté, pas publié** — c'était un bogue d'interpolation linéaire dans la valorisation, qui gonflait le résultat de 10 à 50 fois.
- **Limites des sources de données vérifiées en direct, jamais supposées** : un flux IEX plus court que documenté, une correspondance ticker → CIK erronée dans les données de référence de la SEC elle-même, et un défaut de yfinance qui renvoie silencieusement des prix ajustés plutôt que les prix réellement négociés.
- **Pipeline de données** : fondamentaux trimestriels XBRL de SEC EDGAR, barres de prix et chaînes d'options Alpaca, historique de surprises de résultats Alpha Vantage, avec mise en cache pour ne jamais redépenser un quota.
- **Tests** : suite `pytest` sur le moteur de backtest, les garde-fous d'ordres, le détecteur de régime et les données de résultats.

👉 **[La méthodologie (`lessons_learned.md`)](https://github.com/MinaSeliman1/trading-bot/blob/master/lessons_learned.md)** — le fichier le plus réutilisé du dépôt

---

### [StockLab](https://github.com/MarcSaad-Hadidi/StockLab) — projet de session, équipe de trois

Une plateforme de simulation boursière multinuage, développée en approche agile.

Je suis **responsable du back-end** : conception et développement de l'API REST en **ASP.NET Core** avec **Entity Framework Core**, implémentation de la logique de portefeuille et du moteur de transactions, modélisation et exploitation de la base **Azure SQL**.

Je contribue aussi à l'architecture **multinuage** (Azure + AWS : Service Bus, Lambda, S3, SQS), à l'intégration de l'API boursière Twelve Data, et au raccordement d'un module d'apprentissage automatique en Python qui estime les tendances des titres.

---

## 🛠️ Stack

**Langages**
`C#` · `Python` · `TypeScript` · `JavaScript` · `Java` · `SQL` · `HTML` · `CSS`

**Back-end et données**
`ASP.NET Core (.NET 9)` · `Entity Framework Core` · `API REST` · `PostgreSQL` · `Azure SQL` · `Node.js` · `Authentification JWT` · `Conception de schémas et migrations` · `Architecture en couches et n-tiers`

**Front-end**
`React` · `TypeScript` · `Vite` · `HTML/CSS` · `.NET MAUI` · `XAML`

**Données et analyse**
`pandas` · `NumPy` · `scikit-learn` · `SciPy` · `Matplotlib` · `pyarrow` · `API SEC EDGAR (XBRL)` · `validation walk-forward`

**Qualité et déploiement**
`xUnit` · `pytest` · `Tests unitaires et d'intégration` · `GitHub Actions` · `Docker` · `Git` · `Render` · `Supabase` · `Postman` · `Visual Studio`

**Infonuagique**
`Microsoft Azure` · `AWS (S3, Lambda, SQS)` · `Linux` · `Windows`

**Méthodes**
`Agile` · `Modélisation UML` · `Intégration continue` · `MVVM` · `Injection de dépendances` · `Sécurité applicative`

---

## 📌 Projets

| Projet | Description | Stack |
|---|---|---|
| **[Vigie](https://github.com/MinaSeliman1/vigie)** — [démo](https://minaseliman1.github.io/vigie/) | Gestion de quarts pour équipes de sauveteurs : horaires, échanges approuvés, suivi des certifications. Conçu, développé et déployé seul — 47 endpoints, 70 tests, architecture en quatre couches, CI/CD. | ASP.NET Core · EF Core · PostgreSQL · React · TypeScript · xUnit · GitHub Actions · Render |
| **[Trading Bot Research](https://github.com/MinaSeliman1/trading-bot)** | Recherche quantitative : quatre stratégies testées en validation walk-forward et multi-régimes, quatre rejetées. Le livrable est la méthodologie, pas une stratégie. | Python · pandas · NumPy · scikit-learn · SciPy · pytest · SEC EDGAR · Alpaca |
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

Ouvert aux stages en développement logiciel, web, back-end, données ou infonuagique dans la région de Montréal et Laval.
