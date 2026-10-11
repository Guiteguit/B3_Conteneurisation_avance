# Module 02 — Dockerfile avancé

## Contexte

NovaCorp dispose d'une petite API Python.

Votre objectif est de construire une image Docker propre et optimisée.

---

# Application

L'application se trouve dans :

```text
02-dockerfile/app/
```

---

# TP02 — Construire une image propre

## Partie A — Première image

Créez un Dockerfile capable de lancer l'application.

Contraintes :

- utiliser une image Python officielle ;
- installer les dépendances ;
- exposer le port utilisé par l'application ;
- lancer l'application automatiquement.

Test attendu :

```bash
curl http://localhost:8000
```

---

## Partie B — Analyse

Analysez votre image avec :

```bash
docker history
docker images
```

Relevez :

- la taille totale ;
- le nombre de layers ;
- les layers les plus lourds.

---

## Partie C — Optimisation

Améliorez votre Dockerfile.

Vous devez utiliser au moins quatre des techniques suivantes :

- `.dockerignore` ;
- image `slim` ;
- ordre des layers ;
- cache des dépendances ;
- utilisateur non-root ;
- multi-stage build ;
- suppression des caches ;
- `ENTRYPOINT` ou `CMD` correctement choisi.

Objectif :

> Réduire la taille de l'image sans casser l'application.

---

## Partie D — Cache

Modifiez uniquement une ligne du code Python.

Rebuild.

Observez quelles étapes sont réutilisées depuis le cache.

Modifiez ensuite `requirements.txt`.

Comparez.

Expliquez pourquoi l'ordre des instructions dans un Dockerfile est important.

---

# Livrable

Conservez :

```text
Dockerfile
.dockerignore
```

Ajoutez un fichier :

```text
analyse-image.md
```

contenant :

- taille initiale ;
- taille finale ;
- optimisations réalisées ;
- justification de chaque optimisation.

---

# Challenge

Faites fonctionner l'application dans un conteneur sans que le processus applicatif ne soit exécuté avec l'UID 0.
