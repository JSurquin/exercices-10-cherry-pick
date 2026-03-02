# TP 3.2 – Cherry-pick 🍒

## Ce qui est préconfiguré dans ce dépôt

- **`feature/experimental`** : contient 3 commits :
  1. `feat: add feature A` → `feature-a.txt`
  2. `feat: add feature B` → `feature-b.txt`
  3. `feat: add feature C` → `feature-c.txt`

## Tâches

1. Cloner le dépôt, se placer sur `main`
2. Voir les commits de `feature/experimental` : `git log feature/experimental --oneline`
3. Récupérer le hash du commit `feat: add feature B`
4. Cherry-picker ce commit sur `main` : `git cherry-pick <hash>`
5. Vérifier que `feature-b.txt` est présent sur `main` mais PAS `feature-a.txt` ni `feature-c.txt`
6. Créer une branche `hotfix/urgent` et y cherry-picker le même commit
7. Comparer les hashes : le cherry-pick crée un **nouveau commit** avec un hash différent

## Pourquoi cherry-pick ?

Cherry-pick permet d'appliquer un commit précis d'une branche à une autre **sans merger toute la branche**.
Utile pour porter un correctif urgent vers une branche de prod sans embarquer toutes les features en cours.
