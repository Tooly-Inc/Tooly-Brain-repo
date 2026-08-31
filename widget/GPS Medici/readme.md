# 📝 Widget Tâches & Sous-tâches Hiérarchiques (Zoho CRM)

Ce widget personnalisé offre une interface dynamique pour gérer les **Tâches personnalisées** au sein de Zoho CRM. Il permet de visualiser les relations parents-enfants et de mettre à jour les informations critiques sans quitter la fiche principale.

---

## 🌟 Fonctionnalités

* **Arborescence Dynamique** : Visualisation claire des niveaux de sous-tâches avec boutons de déploiement (+/−).
* **Édition "Inline"** : Modification instantanée du **Statut** et de la **Priorité** via des listes déroulantes intégrées.
* **Compteur de Progression Récursif** : Calcul automatique (ex: `2/5`) du nombre de sous-tâches terminées, incluant tous les sous-niveaux.
* **Feedback Visuel** :
    * Barrage automatique des tâches complétées.
    * Badge de progression qui devient **vert** une fois l'objectif atteint (100%).
    * Effet de transparence lors de la sauvegarde (anti-double clic).
* **Création simplifiée** : Bouton d'accès rapide pour générer de nouvelles tâches via la fenêtre native de Zoho.

---

## 🛠️ Spécifications Techniques

Le widget s'appuie sur le **Zoho JS SDK 1.5** et communique avec le module `T_ches_personnalis_es`.

### Configuration des Champs (API)
| Champ Fonctionnel | Nom API utilisé |
| :--- | :--- |
| **Module Principal** | `T_ches_personnalis_es` |
| **Sujet** | `Name` |
| **Statut** | `Statut` |
| **Priorité** | `Priorit` |
| **Date d'échéance** | `Date_d_ch_ance` |
| **Sous-formulaire** | `Sous_t_ches` |
| **Lookup (dans subform)** | `T_ches` |

### Compatibilité Multi-Module
Le widget détecte automatiquement son contexte et filtre les tâches selon le module parent :
* **Familles** (Accounts) via le champ `Famille`.
* **Comptes** (CustomModule Comptes) via le champ `Compte`.
* **Contacts** via le champ `Client_Contact`.

---

## 📖 Guide d'Utilisation

1.  **Navigation** : Cliquez sur le nom d'une tâche pour ouvrir sa fiche détaillée.
2.  **Déploiement** : Utilisez les boutons bleus à gauche des noms pour explorer les sous-niveaux.
3.  **Mise à jour** : Sélectionnez une nouvelle valeur dans les colonnes *Priorité* ou *Statut*. La sauvegarde est automatique.
4.  **Progression** : Le compteur `x/y` en colonne 2 indique l'état d'avancement global de la branche.

---

