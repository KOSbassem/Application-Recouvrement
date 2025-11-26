# 📌 Application de Recouvrement  
*Documentation officielle du projet *

L’application de recouvrement permet aux entreprises de suivre les factures impayées, automatiser les relances, gérer les paiements, et analyser la performance des agents de recouvrement.

---

## ✨ Fonctionnalités principales

- Suivi des factures impayées  
- Gestion des relances : appel, email, SMS, visite terrain  
- Tableau de bord dynamique  
- Gestion des paiements (espèces, chèques, virements…)  
- Bordereaux pour le service finance  
- Notifications automatiques  
- Historique complet des actions  
- Rapports et statistiques (PDF, Excel)

---

## 🏗 Architecture Générale

L’architecture suit un modèle **Clean Architecture + micro-services légers**.

📄 Voir documentation :  
👉 `/docs/architecture.md`

---

## 🧰 Technologies utilisées

| Couche | Technologie |
|-------|-------------|
| Frontend | Vue.js 3, Vue Router, Axios |
| Backend | Spring Boot (WebFlux, Security, JPA) |
| Base de données | PostgreSQL |
| Authentification | JWT |
| Notifications | WebSocket / Polling |
| Build | Maven + Node.js |
| Déploiement | Docker / NGINX |

📄 Voir documentation :  
👉 `/docs/technologies.md`

---

## 🎨 Design System — UI/UX

L’interface suit une charte moderne orientée SaaS.

| Usage | Couleur |
|--------|---------|
| Primaire | `#2563eb` (Bleu SaaS) |
| Primaire Foncé | `#1e3a8a` |
| Secondaire | `#3b82f6` |
| Danger | `#ef4444` |
| Succès | `#22c55e` |
| Warning | `#eab308` |
| Fond clair | `#f8fafc` |
| Fond sombre | `#0f172a` |

📄 Voir documentation :  
👉 `/docs/design-system.md`

---

## 🚀 Installation & Utilisation

##🔧 Backend

cd backend
mvn spring-boot:run

## 🖥 Frontend
cd frontend
npm install
npm run serve

docker run --name ****** -p 5432:5432 -e POSTGRES_PASSWORD=*** -d postgres

📊 Documentation technique

📁 Dossier /docs :

    scenario-general.md → Définition du projet

    fonctionnalites.md → Fonctionnalités détaillées

    architecture.md → Architecture du système

    modelisation-bdd.md → Modèle de base de données

    design-system.md → UI/UX & couleurs

    roadmap.md → Roadmap projet

    screenshots → Images de l'app

🧪 Tests

Tests unitaires (JUnit)

Tests E2E (Postman)

Tests UI (Cypress)


# 🔥 2️⃣ **docs/overview.md**

# 🧾 Présentation générale du projet

L’application de recouvrement digitalise totalement le suivi des factures impayées et le travail des agents de recouvrement.

Elle remplace les méthodes classiques (Excel, carnets papier, emails manuels) par une plateforme centralisée.

## Objectifs
- Améliorer la visibilité sur les impayés  
- Automatiser les relances  
- Réduire les délais de paiement  
- Assurer un suivi fiable et centralisé  
- Permettre une communication entre Recouvrement → Caisse → Finance
