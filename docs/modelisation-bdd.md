# 🗄 Modélisation + Architecture + Interactions entre Composants

Ce document présente :
- le modèle de base de données,
- l’architecture globale,
- les interactions entre les modules du système.

---

# 1️⃣ Architecture Globale du Système

L’application de recouvrement repose sur **4 composants principaux** :


### 🔄 Interaction entre les composants

| Composant | Rôle |
|----------|------|
| **Frontend (Vue.js)** | Interface utilisateur, appels API, affichage données |
| **Backend (Spring Boot)** | Logique métier, sécurité, relances, paiements |
| **PostgreSQL** | Stockage factures, paiements, relances, bordereaux |
| **Navision** | Source externe des factures & clients |

### ⚙️ Flux normal d'utilisation

1. Navision envoie les factures → Backend → PostgreSQL  
2. L’agent se connecte sur le Frontend  
3. Le Frontend appelle l’API Spring Boot  
4. Spring Boot lit/écrit dans PostgreSQL  
5. Paiements → Bordereaux → Validation Finance  
6. Historique et rapports générés depuis PostgreSQL  

---



