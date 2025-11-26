# 📘 Scénario Général de l’Application de Recouvrement

## 🎯 Objectif Général
L'application a pour mission de digitaliser et automatiser le processus de recouvrement pour améliorer la récupération des
factures impayées, optimiser le travail des agents et faciliter les échanges avec le service financier.

Elle permet :
- le suivi complet des factures impayées,
- la gestion des relances clients,
- l’enregistrement des paiements,
- la génération de bordereaux,
- et la production de rapports financiers.

---

# 👥 1. Gestion des Utilisateurs & Authentification

### Rôles existants
| Rôle | Permissions principales |
|------|--------------------------|
| **Admin** | Gestion utilisateurs, configuration globale |
| **Agent Recouvrement** | Relances, paiements, suivi client |
| **Caissier** | Encaissements et gestion des bordereaux |
| **Finance** | Vérification, validation et reporting |

### Fonctionnalités
- Connexion via email + mot de passe
- Sessions sécurisées (JWT)
- Réinitialisation mot de passe par email
- Définition des permissions par rôle

---

# 📊 2. Dashboard – Vue Globale du Recouvrement

Le tableau de bord présente :
- montant total des impayés,
- nombre de factures en retard,
- paiements réalisés,
- top clients débiteurs,
- taux de recouvrement,
- alerts automatiques.

Fonctionnalités :
✔ Tri  
✔ Filtres intelligents  
✔ Accès direct aux clients ou factures concernées  

---

# 👤 3. Gestion des Clients

Chaque fiche client permet :
- de visualiser toutes les factures impayées,
- de consulter l’historique complet des relances,
- de suivre les paiements enregistrés,
- de calculer le solde global du client,
- d'afficher des alertes liées au comportement de paiement.

Filtres :
- nom / ID,
- montant impayé,
- statut du recouvrement,
- dernière relance.

---

# 📑 4. Gestion des Factures

Une facture contient :
- n° facture,
- client,
- montant total,
- montant réglé,
- solde restant,
- statut (payée/partielle/en retard),
- date de relance prévue.

Actions :
- enregistrer un paiement,
- programmer une relance,
- associer à un bordereau,
- consulter l’historique complet.

---

# 📞 5. Relances Clients

Types de relances :
1. Appel téléphonique  
2. Email de rappel  
3. Message WhatsApp  
4. Visite terrain  

Pour chaque relance :
- compte-rendu obligatoire,
- statut du résultat,
- promesse éventuelle,
- date de prochaine relance automatique.

Notifications :
- relances prévues aujourd'hui,
- relances en retard,
- clients à risque élevé.

---

# 💰 6. Paiements

Modes disponibles :
- Espèce
- Chèque
- Virement
- Traite
- Paiement mixte

Chaque paiement :
✔ réduit automatiquement les impayés  
✔ peut être affecté à plusieurs factures  
✔ génère un bordereau automatiquement pour le caissier  

---

# 📄 7. Bordereaux

Un bordereau regroupe :
- les paiements,
- les moyens de paiement associés,
- les montants encaissés.

Statuts d’un bordereau :
- **En attente**
- **Validé**
- **Rejeté**

Export possible :
- PDF  
- Excel  

---

# 🔔 8. Notifications

Types :
- relances du jour,
- nouvelles factures clients,
- validation bordereau,
- paiement reçu,
- factures dépassant un seuil X jours.

---

# 📈 9. Rapports & Statistiques

Rapports disponibles :
- factures en retard par agent,
- paiements reçus par période,
- historique du taux de recouvrement,
- clients avec dettes importantes.

Exports :
✔ PDF  
✔ Excel  

---

# ✔ Conclusion

Ce scénario global sert de **référence fonctionnelle** pour comprendre l’ensemble du cycle de recouvrement.  
Il décrit de manière claire les modules nécessaires pour développer une application complète et moderne.
