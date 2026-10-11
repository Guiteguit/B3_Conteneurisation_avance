# Module 09 — CI/CD Docker

## Objectif

NovaCorp ne veut plus construire les images manuellement sur un poste administrateur.

Vous devez automatiser le processus.

---

# TP09 — Pipeline de build

Le dépôt doit déclencher une CI lors d'un push.

La CI doit au minimum :

```text
checkout
  |
  v
validation
  |
  v
docker build
```

---

## Niveau 1 — Obligatoire

Créez un workflow GitHub Actions qui :

1. récupère le dépôt ;
2. construit l'image ;
3. vérifie que le build réussit.

---

## Niveau 2 — Recommandé

Ajoutez :

- tag automatique ;
- scan de sécurité ;
- cache de build.

---

## Niveau 3 — Bonus

Publiez automatiquement l'image vers :

- GitHub Container Registry ;
- ou un registry de votre choix.

Ne mettez aucun mot de passe directement dans le workflow.

---

# Travail demandé

Votre workflow doit se trouver dans :

```text
.github/workflows/
```

Vous devez être capables d'expliquer :

- ce qui déclenche le pipeline ;
- où s'exécutent les commandes ;
- comment sont stockés les secrets ;
- ce qui se passe en cas d'échec.

---

# Livrable

Ajoutez :

```text
ci-cd.md
```

avec :

- schéma du pipeline ;
- déclencheurs ;
- étapes ;
- captures ou résultats d'exécution ;
- problèmes rencontrés.

---

# Challenge

Empêchez la publication d'une image si l'étape de validation échoue.
