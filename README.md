# 🧾 Kerkonia – Plateforme de Caisse Open Source pour la Restauration

![Logo Kerkonia](https://avatars.githubusercontent.com/u/213294475?s=200\&v=4)

> Un projet libre, structuré en modules, pour offrir à la restauration une technologie moderne, interconnectée, souveraine et accessible à tous. Une réponse concrète à un marché verrouillé, conçue pour faire évoluer les standards techniques et juridiques de la FoodTech.

---

## 🧠 Pourquoi Kerkonia ?

**Kerkonia** est né d’un besoin vital : offrir aux restaurateurs un contrôle total sur leurs outils technologiques.
Trop d’acteurs sont enfermés dans des solutions propriétaires coûteuses, obsolètes ou inadaptées, qui les empêchent de croître sereinement ou d’adapter leur service à leurs besoins spécifiques.

Ce projet est aussi un **acte de résilience et d’innovation**, né d’une volonté forte de **relever un défi personnel et professionnel** après un conflit avec mon ancien employeur. L’idée : transformer l’injustice en moteur créatif. Donner aux autres ce qu’on m’a refusé : **la liberté, la transparence, et la performance.**

Kerkonia incarne une vision ambitieuse, communautaire et inclusive :

* ✅ **Gratuit** : aucune redevance ni verrou commercial
* ✅ **Open source** : chaque ligne de code peut être audité, amélioré, partagé
* ✅ **Modulaire** : chaque brique est indépendante, réutilisable, évolutive
* ✅ **Technologiquement fiable** : basé sur des standards modernes (Symfony, Laravel, Docker, Vue.js)
* ✅ **Légalement conforme** : pensé pour les réglementations fiscales, RGPD, HACCP, et demain, certifié par l’État

> Kerkonia n’est pas une alternative. C’est **une nouvelle norme.**

---

## 📌 Informations légales

* **Auteur** : BEN MECHA Ali *(société Kerkonia)*
* **SIRET** : 943 224 774 00017
* **Licence** : AGPL-3.0 – Code libre à condition de maintenir la même liberté dans les dérivés redistribués
* **Dépôt principal** : [https://github.com/kerkonia](https://github.com/kerkonia)

---

## 🪸 Origine du nom et logo

Le nom **Kerkonia** fusionne mes racines **kerkanniennes** (Kerkennah, Tunisie) avec une identité numérique forte.
Le logo représente **un palmier stylisé et une plage** — symboles d’ancrage, de sérénité, mais aussi d’ouverture sur le monde.

Ce projet s’inscrit dans une logique de rayonnement, inspiré par **la harissa**, la chaleur humaine, la culture méditerranéenne. Il est le grand frère technique du projet [PEPRIO](https://pepprio.com), dédié à l’agrégation de plateformes de livraison.

> Kerkonia est une déclaration d'indépendance technologique.

---

## 🧱 Architecture modulaire complète

Chaque couche de Kerkonia a été pensée pour être **interchangeable, testable, distribuée** :

```text
                       +--------------------------+
                       |    Interface Utilisateur  |
                       |      Vue.js + Tailwind    |
                       +--------------------------+
                                |
                 +--------------+---------------+
                 |                              |
       +------------------+           +---------------------+
       | App Mobile Ionic |           |  App Desktop (POS)  |
       | Capacitor + Vue  |           |  Electron + Vue     |
       +------------------+           +---------------------+
                 |                              |
                 +--------------+---------------+
                                |
                                v
              +-----------------------------------------+
              |     Laravel API – Modules & Plugins     |
              | Menu, Paiement, IA, Market, Extensions  |
              +-----------------------------------------+
                                |
                                v
              +-----------------------------------------+
              |   Symfony API – Noyau Métier (Core)     |
              | Commandes, Utilisateurs, Événements     |
              +-----------------------------------------+
                                |
                                v
                    +----------------------------+
                    |      Base de Données       |
                    +----------------------------+
```

---

## 📂 Repositories (cliquables, détaillés)

Chaque dépôt est autonome, interconnectable et documenté.

| Repository                                                                               | Description détaillée                                                               | Stack                     |
| ---------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ------------------------- |
| [`kerkonia-core`](https://github.com/kerkonia/kerkonia-core)                             | Cœur Symfony : gestion des rôles, permissions, menus, commandes, webhooks, sécurité | `Symfony`                 |
| [`kerkonia-plugin-stripe`](https://github.com/kerkonia/kerkonia-plugin-stripe)           | Paiement Stripe : frais réduits, intégration checkout, gestion webhooks             | `Laravel`, `Stripe API`   |
| [`kerkonia-plugin-ubereats`](https://github.com/kerkonia/kerkonia-plugin-ubereats)       | SDK PHP + webhook manager pour intégrer Uber Eats à la caisse                       | `PHP`, `Laravel`, `OAuth` |
| [`kerkonia-plugin-deliveroo`](https://github.com/kerkonia/kerkonia-plugin-deliveroo)     | SDK PHP pour connexion bidirectionnelle Deliveroo (menu + commandes)                | `PHP`                     |
| [`kerkonia-module-menu`](https://github.com/kerkonia/kerkonia-module-menu)               | Interface centrale de gestion multi-menus, multi-devise, multi-TVA, multi-site      | `Laravel`, `REST`         |
| [`kerkonia-module-kds`](https://github.com/kerkonia/kerkonia-module-kds)                 | Écran cuisine : dispatch commandes, gestion des zones, retour état cuisson          | `Vue.js`, `WebSocket`     |
| [`kerkonia-module-bornes`](https://github.com/kerkonia/kerkonia-module-bornes)           | Kiosques clients : navigation, panier, paiement, fidélité                           | `Vue.js`, `Capacitor`     |
| [`kerkonia-module-marketplace`](https://github.com/kerkonia/kerkonia-module-marketplace) | Site web complet pour prise de commande (type Uber/Deliveroo sans commission)       | `Laravel`, `Vue.js`       |
| [`kerkonia-module-paiement`](https://github.com/kerkonia/kerkonia-module-paiement)       | TPE (SumUp, Zettle), paiements QR/NFC, Stripe Terminal                              | `Laravel`, `WebBluetooth` |
| [`kerkonia-module-ai`](https://github.com/kerkonia/kerkonia-module-ai)                   | Moteur d’IA : prédiction vente, image plat, calendrier intelligent, prix dynamique  | `Python`, `Node.js`       |
| [`kerkonia-mobile-app`](https://github.com/kerkonia/kerkonia-mobile-app)                 | Application mobile : prise de commande, scan QR, gestion fidélité                   | `Ionic`, `Vue.js`         |
| [`kerkonia-desktop-app`](https://github.com/kerkonia/kerkonia-desktop-app)               | Application de caisse Windows/Mac/Linux (connectée en local)                        | `Electron`, `Vue.js`      |
| [`kerkonia-sdk-php`](https://github.com/kerkonia/kerkonia-sdk-php)                       | SDK d’intégration avec d’autres systèmes PHP (middleware, CMS, etc.)                | `PHP`, `Composer`         |
| [`kerkonia-sdk-typescript`](https://github.com/kerkonia/kerkonia-sdk-typescript)         | SDK TypeScript pour intégration front (SPA/PWA/Capacitor)                           | `TypeScript`              |

---

## 🛠️ Déploiement rapide (Docker Dev)

```bash
git clone https://github.com/kerkonia/kerkonia-core.git
cd kerkonia-core
cp .env.example .env
docker-compose up -d --build
```

🌐 Accès : [localhost:8080](http://localhost:8080)
🔐 Admin par défaut : `admin@kerkonia.dev` / `changeme`

➡️ Doc complète bientôt sur **[https://kerkonia.dev](https://kerkonia.dev)**

---

## ✅ Conformité légale et ambition juridique

Kerkonia est conçu pour répondre à :

* ✅ RGPD : suppression, consentement, audit des données
* ✅ HACCP : traçabilité, hygiène, alertes produit
* ✅ Archivage fiscal : format sécurisé, journalisation inaltérable
* ✅ Signature blockchain & identifiants numériques
* 📑 Certification fiscale (procédure en cours auprès de l'administration française)
* 📚 Manuel utilisateur téléchargeable (version PDF certifiée)

---

## 🤖 IA & Intelligence augmentée (module AI)

* 📷 Génération automatisée d’images pour Uber/Deliveroo/Open Graph
* 🧠 Suggestions de menus en fonction des événements, météo, tendances locales
* 📊 Analyse de performance (plat, heure, jour, panier moyen, marge)
* 🛎️ Alertes automatiques (rupture, lenteur préparation)
* 🎯 Prix dynamiques en temps réel selon contexte et objectifs

---

## 🚀 Pourquoi rejoindre Kerkonia ?

Ce projet est **plus qu’un logiciel** : c’est un manifeste. Une révolte constructive. Un outil d’émancipation technologique.

Si vous êtes :

* 🍽️ Restaurateur fatigué des solutions imposées
* 👨‍💻 Développeur passionné de Laravel, Symfony, Vue
* 🛠️ Intégrateur de matériel ou prestataire IT
* 🧠 Ingénieur IA ou designer d'expérience
* 🤝 Investisseur tech éthique

📬 Contact : [contact@benmacha.tn](mailto:contact@benmacha.tn)

---

> 🔹 **Kerkonia** – Une caisse libre, fiable, modulaire, communautaire.
> Ce que d'autres verrouillent, nous l’ouvrons.
