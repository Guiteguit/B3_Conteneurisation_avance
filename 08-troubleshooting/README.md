# Module 08 — Troubleshooting et observabilité

## Objectif

Une application conteneurisée qui démarre n'est pas forcément fonctionnelle.

Votre objectif est d'adopter une méthode de diagnostic.

---

# TP08 — Diagnostic NovaCorp

## Méthode imposée

Pour chaque incident, suivez :

```text
1. Symptôme
2. Hypothèses
3. Vérifications
4. Cause racine
5. Correction
6. Validation
```

Ne corrigez pas avant d'avoir identifié la cause.

---

# Incident A

Le conteneur API est :

```text
Up
```

mais :

```bash
curl http://localhost
```

retourne une erreur.

Vous devez déterminer si le problème vient de :

- nginx ;
- réseau ;
- API ;
- port ;
- DNS Docker.

---

# Incident B

La base redémarre régulièrement.

Trouvez la cause avec :

```text
logs
inspect
events
stats
```

---

# Incident C

L'API répond mais certaines requêtes sont très lentes.

Observez :

- CPU ;
- mémoire ;
- logs ;
- réseau ;
- processus.

---

# Outils à connaître

Vous devez maîtriser :

```bash
docker ps
docker logs
docker inspect
docker stats
docker top
docker events
docker network inspect
docker compose logs
curl
ss
ip
```

Ajoutez vos propres outils utiles.

---

# Bonus observabilité

Déployez `cAdvisor`.

Observez les métriques disponibles.

Identifiez au minimum :

- utilisation CPU ;
- mémoire ;
- trafic réseau ;
- filesystem.

Aucun dashboard Grafana n'est obligatoire.

---

# Livrable

Créez :

```text
troubleshooting.md
```

Décrivez les incidents rencontrés et votre méthode.

---

# Challenge

Construisez une commande permettant d'afficher rapidement :

```text
nom du conteneur
état
CPU
RAM
```

pour tous les conteneurs NovaCorp.
