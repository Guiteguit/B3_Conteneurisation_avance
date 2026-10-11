# Module 07 — Registry et cycle de vie des images

## Objectifs

Vous allez publier et récupérer vos propres images.

---

# TP07 — Registry NovaCorp

## Partie A — Registry local

Déployez un registry Docker local basé sur l'image officielle :

```text
registry:2
```

Il doit être accessible sur votre machine.

---

## Partie B — Tag

Construisez l'image NovaCorp puis créez plusieurs tags :

```text
1.0.0
1.0
latest
```

Expliquez la différence entre :

```text
tag
digest
```

---

## Partie C — Push

Publiez votre image dans votre registry local.

Supprimez ensuite l'image locale.

Téléchargez-la à nouveau depuis le registry.

---

## Partie D — Versioning

Simulez une version :

```text
1.1.0
```

Modifiez l'API afin qu'elle expose cette version.

Publiez la nouvelle image.

---

## Questions

1. Pourquoi `latest` est-il dangereux en production ?
2. Pourquoi utiliser un digest ?
3. Que se passe-t-il si un tag existant est réutilisé ?
4. Quelle différence entre Docker Hub et un registry privé ?
5. Pourquoi scanner une image avant publication ?

---

# Livrable

Créez :

```text
registry.md
```

avec :

- adresse du registry ;
- images publiées ;
- stratégie de tags ;
- procédure de rollback vers la version précédente.

---

# Challenge

Déployez `1.1.0`, puis revenez à `1.0.0` sans rebuild.
