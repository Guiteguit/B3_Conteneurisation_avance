# Module 04 — Stockage et persistance

## Contexte

L'équipe NovaCorp découvre que supprimer un conteneur peut entraîner la perte de données.

Votre objectif est de rendre les données persistantes.

---

# TP04 — PostgreSQL persistant

## Partie A — Sans volume

Lancez PostgreSQL dans un conteneur.

Créez :

- une base ;
- une table ;
- quelques données.

Supprimez ensuite le conteneur.

Recréez-le avec la même image.

Que deviennent les données ?

---

## Partie B — Named Volume

Recommencez en utilisant un volume Docker nommé :

```text
novacorp-db-data
```

Vérifiez que les données survivent à la suppression du conteneur.

---

## Partie C — Inspection

Identifiez :

- l'emplacement du volume ;
- le type de mount ;
- la destination dans le conteneur.

Utilisez notamment :

```bash
docker volume inspect
docker inspect
```

---

## Partie D — Bind Mount

Montez un répertoire de l'hôte dans un conteneur.

Comparez :

```text
bind mount
named volume
```

Indiquez dans quels cas vous utiliseriez chacun.

---

## Partie E — Sauvegarde

Vous devez proposer une procédure permettant de :

1. sauvegarder la base PostgreSQL ;
2. supprimer le conteneur ;
3. recréer la base ;
4. restaurer les données.

Vous pouvez utiliser `pg_dump`, `pg_restore` ou `psql`.

---

# Livrable

Créez :

```text
storage.md
```

avec :

- votre méthode de persistance ;
- votre méthode de sauvegarde ;
- votre méthode de restauration ;
- la différence entre volume et bind mount ;
- les commandes utilisées.

---

# Challenge

Expliquez pourquoi sauvegarder uniquement le répertoire du volume PostgreSQL « à chaud » peut être risqué.
