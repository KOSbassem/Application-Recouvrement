# 🏗 Architecture Technique – Application de Recouvrement

## 1. Vue d’ensemble

L’architecture repose sur une séparation claire :
- **Frontend** : Vue.js
- **Backend** : Spring Boot (REST API)
- **Base de données** : PostgreSQL
- **ERP externe** : Microsoft Dynamics Navision / Business Central
- **Authentification** : JWT

![architecture](../assets/screenshots/architecture.png)

---

# 2. Architecture Frontend (Vue.js)

### Structure principale
- `src/components` → composants
- `src/views` → pages
- `src/router` → routing
- `src/services` → appels API
- `src/assets` → images & styles

### Modules principaux
- Dashboard
- Gestion Clients
- Gestion Factures
- Paiements
- Bordereaux
- Notifications
- Authentification

---

# 3. Architecture Backend (Spring Boot)

### Modules techniques
| Module | Description |
|--------|-------------|
| `auth` | Gestion JWT, login |
| `clients` | Gestion des clients |
| `factures` | Import, suivi, statuts |
| `paiements` | Enregistrement, validation |
| `relances` | Programmation, historique |
| `notifications` | Système d’alertes |
| `bordereaux` | Génération & validation |

### Technologies
- Spring Web
- Spring Security (JWT)
- Spring Data JPA
- PostgreSQL Driver
- Lombok
- MapStruct

---

# 4. Base de Données (PostgreSQL)

Tables principales :
- clients
- factures
- paiements
- relances
- bordereaux
- utilisateurs
- roles
- notifications

Schéma simplifié :
![bdd](../assets/screenshots/bdd.png)

---

# 5. Intégration Navision

Synchronisation automatique :
- import des factures,
- import des clients,
- mise à jour des paiements validés,
- récupération des soldes clients.

Méthode :
- API REST Navision
- ou Web Services (SOAP/ODATA)

---

# 6. Sécurité

- JWT Access Token
- Refresh Token
- Rôles + Permissions
- CORS configuré pour le frontend

---

# 7. Déploiement

### Environnement recommandé
| Composant | Technologie |
|----------|-------------|
| Backend | Spring Boot (Jar) |
| Frontend | Nginx (dist folder) |
| BDD | PostgreSQL |
| Monitoring | Grafana + Prometheus |

CI/CD :
- GitHub Actions pour build & test
- Docker pour standardisation

---

# ✔ Conclusion

L’architecture est conçue pour être :
✔ évolutive  
✔ modulaire  
✔ performante  
✔ compatible ERP  
✔ sécurisée  

Elle pose une base solide pour tout développement futur.
