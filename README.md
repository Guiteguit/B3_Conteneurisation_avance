# B3_SRC_26_1 — T1 : Conteneurisation avancée

## Présentation

Ce dépôt contient le parcours étudiant du module **Conteneurisation avancée**.

Durée totale : **15 heures**  
Organisation : **10 modules de 1 h 30**  
Public : **Bachelor 3 SRC**  
Travail conseillé : **binômes**

Le cours est basé sur un fil rouge : **NovaCorp**, une petite application web que vous allez progressivement conteneuriser, connecter, sécuriser, superviser et industrialiser.

---

## Architecture cible

```text
Utilisateur
    |
    v
+---------+
|  Nginx  |
+----+----+
     |
     v
+---------+
| FastAPI |
+----+----+
     |
     v
+------------+
| PostgreSQL |
+------------+
```

Au début du cours, cette architecture sera volontairement très simple.

Vous devrez progressivement :

- comprendre ce qu'est réellement un conteneur ;
- créer et optimiser des images ;
- construire des réseaux Docker ;
- gérer la persistance ;
- orchestrer plusieurs services avec Docker Compose ;
- sécuriser une stack ;
- publier des images dans un registry ;
- diagnostiquer des incidents ;
- automatiser la construction d'images ;
- résoudre un incident final.

---

# Règles de travail

Les TPs ne sont volontairement pas des procédures à copier-coller.

Vous devez :

1. analyser le besoin ;
2. rechercher les commandes adaptées ;
3. tester ;
4. observer ;
5. expliquer vos choix ;
6. conserver les commandes importantes dans vos notes.

La validation ne repose pas uniquement sur le fait que « cela fonctionne ».

Vous devez être capables d'expliquer **pourquoi cela fonctionne**.

---

# Progression

| Module | Sujet |
|---|---|
| 00 | Préparation de l'environnement |
| 01 | Internals et cycle de vie |
| 02 | Dockerfile avancé |
| 03 | Networking |
| 04 | Stockage et persistance |
| 05 | Docker Compose |
| 06 | Sécurité |
| 07 | Registry |
| 08 | Troubleshooting et observabilité |
| 09 | CI/CD |
| 10 | Final Boss |

---

# Compétences visées

À la fin du module, vous devez être capables de :

- expliquer la différence entre une VM et un conteneur ;
- inspecter le fonctionnement d'un conteneur ;
- construire une image Docker propre ;
- optimiser un Dockerfile ;
- concevoir des réseaux Docker ;
- utiliser des volumes persistants ;
- déployer une application multi-conteneurs ;
- appliquer des mesures de sécurité ;
- diagnostiquer un incident ;
- mettre en place une chaîne CI simple pour une image Docker.

---

# Pré-requis

Vous devez disposer d'une machine Linux ou d'une VM Linux avec :

- 4 vCPU minimum ;
- 8 Go de RAM recommandés ;
- 20 Go d'espace disponible ;
- accès Internet ;
- Git ;
- Docker Engine ;
- Docker Compose Plugin.

Distribution recommandée :

```text
Debian 13
ou
Ubuntu 24.04 LTS
```

---

# Important

Le dossier `10-final-boss` contient l'évaluation pratique finale.

Ne cherchez pas une solution toute faite : le but est de démontrer une méthode de diagnostic.
