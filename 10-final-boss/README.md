# Module 10 — FINAL BOSS

# Incident NovaCorp

Votre équipe est appelée sur un incident affectant la plateforme NovaCorp.

La plateforme doit normalement fournir :

```text
Utilisateur
    |
    v
Nginx
    |
    v
FastAPI
    |
    v
PostgreSQL
```

---

# Votre mission

Vous disposez d'un environnement qui contient une ou plusieurs erreurs.

Vous devez :

1. identifier les symptômes ;
2. établir des hypothèses ;
3. diagnostiquer ;
4. trouver les causes racines ;
5. corriger ;
6. valider ;
7. documenter.

---

# Règles

Vous n'avez pas le droit de :

```text
tout supprimer
réinstaller Docker
recréer toute la machine
remplacer tous les fichiers sans analyse
```

Un redémarrage peut être utilisé uniquement s'il est justifié.

---

# Méthode attendue

Votre compte-rendu doit suivre cette structure :

## Symptôme

Que constatez-vous ?

## Hypothèses

Quelles causes envisagez-vous ?

## Tests

Quelles commandes utilisez-vous ?

## Résultats

Qu'observez-vous ?

## Cause racine

Quel était le problème ?

## Correction

Quelle modification avez-vous réalisée ?

## Validation

Comment prouvez-vous que le service fonctionne ?

## Prévention

Que pourrait-on mettre en place pour éviter cet incident ?

---

# Points de contrôle

Votre environnement peut contenir des problèmes liés à :

- build ;
- réseau ;
- DNS ;
- ports ;
- volumes ;
- permissions ;
- healthchecks ;
- ressources ;
- variables ;
- sécurité ;
- registry ;
- configuration Compose.

---

# Livrable final

Créez :

```text
FINAL_REPORT.md
```

Votre rapport doit contenir :

- architecture ;
- symptômes ;
- diagnostic ;
- commandes importantes ;
- cause racine ;
- correction ;
- validation ;
- recommandations.

---

# Important

La note ne dépend pas seulement de la vitesse.

Une bonne démarche de diagnostic vaut plus qu'une correction faite au hasard.
