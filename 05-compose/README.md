# Module 05 — Docker Compose

## Objectif

NovaCorp ne veut plus lancer ses composants avec plusieurs commandes `docker run`.

Vous devez décrire l'ensemble de la stack dans un fichier Docker Compose.

---

# TP05 — Déploiement NovaCorp

Vous devez construire :

```text
Client
  |
  v
nginx
  |
  v
api
  |
  v
postgres
```

---

## Services obligatoires

### nginx

Rôle :

```text
reverse proxy
```

### api

Rôle :

```text
API FastAPI NovaCorp
```

### db

Rôle :

```text
PostgreSQL
```

---

# Contraintes

Votre `compose.yaml` doit contenir :

- trois services ;
- au moins deux réseaux ;
- un volume persistant ;
- des variables d'environnement ;
- une restart policy ;
- au moins un healthcheck ;
- aucune publication directe du port PostgreSQL.

---

## Configuration attendue

L'utilisateur doit accéder à :

```text
http://localhost
```

Nginx transfère ensuite les requêtes vers l'API.

L'API doit connaître :

```text
DB_HOST
DB_NAME
DB_USER
DB_PASSWORD
```

---

## Travail demandé

Vous devez créer :

```text
compose.yaml
nginx.conf
.env.example
```

Le vrai fichier `.env` ne doit pas être commité si vous y placez des secrets.

---

## Commandes à maîtriser

Vous devez savoir expliquer et utiliser :

```bash
docker compose up
docker compose down
docker compose ps
docker compose logs
docker compose exec
docker compose config
```

---

# Validation

Les tests suivants doivent être possibles :

```bash
curl http://localhost/
curl http://localhost/health
```

La base doit rester persistante après :

```bash
docker compose down
docker compose up -d
```

---

# Challenge

Modifiez la stack pour qu'une dépendance à la base ne soit considérée comme prête que lorsque PostgreSQL répond correctement.
