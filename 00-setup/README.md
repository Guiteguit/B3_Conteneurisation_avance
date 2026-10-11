# Module 00 — Préparation de l'environnement

## Objectifs

Avant de commencer, votre poste doit être capable de :

- exécuter Docker ;
- utiliser Docker Compose ;
- cloner un dépôt Git ;
- communiquer avec Internet ;
- exécuter des commandes avec les droits nécessaires.

---

## 1. Vérifications

Vérifiez les versions installées :

```bash
docker --version
docker compose version
git --version
```

Vérifiez l'état du service Docker :

```bash
systemctl status docker
```

Testez le moteur :

```bash
docker run --rm hello-world
```

---

## 2. Travail demandé

Créez un fichier `environment.md` contenant :

- votre distribution ;
- votre version de noyau ;
- votre version Docker ;
- votre version Docker Compose ;
- votre adresse IP ;
- la quantité de RAM disponible ;
- le nombre de CPU disponibles.

Vous devez trouver les commandes permettant d'obtenir ces informations.

---

## 3. Questions

Répondez dans `environment.md` :

1. Docker fonctionne-t-il avec un daemon ?
2. Quel processus correspond au daemon Docker ?
3. Quel utilisateur exécute ce processus ?
4. Pourquoi l'appartenance au groupe `docker` est-elle sensible ?
5. Quelle différence faites-vous entre `docker compose` et l'ancien `docker-compose` ?

---

## Validation

À la fin du module :

```bash
docker ps
docker compose version
```

doivent fonctionner sans erreur.
