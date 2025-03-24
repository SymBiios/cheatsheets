# 🌿 Résumé des Branches dans Gitflow

Gitflow utilise plusieurs types de branches pour organiser le développement d'un projet. Chaque branche a un rôle bien précis :

## 🏛 Branches Principales

### `main`
- Contient **uniquement** du code **stable** et **déployable en production**.
- Chaque mise à jour correspond à une **nouvelle version officielle**.

### `develop`
- Branche où se fait le **développement actif**.
- Regroupe toutes les nouvelles fonctionnalités avant qu'elles ne soient intégrées dans `main`.

---

## 🌱 Branches Auxiliaires

### `feature/*`
- Créées à partir de `develop` pour **développer une nouvelle fonctionnalité**.
- Permettent un travail isolé avant intégration dans `develop`.
- Supprimées une fois fusionnées.

➡️ **Utilité** : Empêche que des fonctionnalités incomplètes perturbent le développement principal.

### `release/*`
- Créées à partir de `develop` pour **préparer une nouvelle version**.
- Permettent d'apporter les dernières corrections avant de passer en production.
- Fusionnées dans `main` et `develop`, puis supprimées.

➡️ **Utilité** : Stabiliser le code avant de le livrer en production.

### `hotfix/*`
- Créées à partir de `main` pour **corriger un bug urgent en production**.
- Une fois corrigées, elles sont fusionnées dans `main` et `develop`.

➡️ **Utilité** : Permet d'apporter des corrections rapides **sans attendre une nouvelle release**.

---

## 🏁 Pourquoi Utiliser ces Branches ?
✅ **Organisation claire** du développement  
✅ **Évite les conflits** entre nouvelles fonctionnalités et corrections urgentes  
✅ **Permet des livraisons stables** en séparant développement et production  
✅ **Facilite le travail en équipe** en définissant un cadre structuré  

💡 **Gitflow est un excellent choix pour les projets collaboratifs ou à long terme !** 🚀
