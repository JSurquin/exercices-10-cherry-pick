# TP 3.2 – Cherry-pick

Appliquer un commit précis d'une branche à une autre.

## Tâches

1. Créer une branche `feature/experimental`
2. Faire **3 commits** (ajouter `feature-a.txt`, `feature-b.txt`, `feature-c.txt`)
3. **Noter le hash** du 2e commit (celui de `feature-b.txt`) : `git log --oneline`
4. Revenir sur `main`
5. Appliquer uniquement ce commit : `git cherry-pick <hash>`
6. Créer `hotfix/urgent` et y appliquer aussi ce commit
7. Vérifier que `feature-b.txt` est présent sur `main`, `feature/experimental` et `hotfix/urgent`

## Astuce

```bash
# Voir le hash d'un commit précis
git log --oneline feature/experimental

# Cherry-pick
git cherry-pick <hash>
```

> Le cherry-pick crée un **nouveau commit** avec un hash différent, mais le même contenu.
