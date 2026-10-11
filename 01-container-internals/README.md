# Module 01 — Comprendre ce qu'est réellement un conteneur

## Contexte

Un conteneur n'est pas une machine virtuelle miniature.

Dans ce module, vous allez observer ce que Docker fait réellement lorsqu'un conteneur est lancé.

---

# TP01 — Container Internals

## Partie A — Premier conteneur

Lancez un conteneur Debian interactif.

À l'intérieur du conteneur :

- affichez les processus ;
- affichez les interfaces réseau ;
- affichez les routes ;
- affichez le hostname ;
- affichez le contenu de `/proc/1/cgroup`.

Depuis l'hôte, retrouvez les mêmes informations autant que possible.

---

## Partie B — PID

Lancez :

```text
un conteneur qui exécute sleep pendant plusieurs minutes
```

Retrouvez :

- son PID dans le conteneur ;
- son PID vu depuis l'hôte.

Expliquez pourquoi les deux valeurs peuvent être différentes.

---

## Partie C — Ressources

Lancez plusieurs conteneurs puis observez :

- CPU ;
- mémoire ;
- processus ;
- limites éventuelles.

Vous devez identifier au minimum quatre commandes Docker permettant d'obtenir ces informations.

---

## Partie D — Filesystem

Dans un conteneur :

1. créez un fichier `/tmp/demo.txt` ;
2. arrêtez le conteneur ;
3. redémarrez-le ;
4. vérifiez la présence du fichier ;
5. supprimez le conteneur ;
6. recréez-en un nouveau depuis la même image.

Que devient le fichier ?

Expliquez la différence entre :

```text
arrêt du conteneur
suppression du conteneur
suppression de l'image
```

---

## Partie E — Inspection

À l'aide de `docker inspect`, retrouvez :

- l'image utilisée ;
- l'adresse IP ;
- le réseau ;
- les mounts ;
- le hostname ;
- les variables d'environnement ;
- la politique de restart.

---

# Livrable

Créez :

```text
01-container-internals/compte-rendu.md
```

avec :

- 5 observations importantes ;
- une explication de la différence VM / conteneur ;
- une explication simple des namespaces ;
- une explication simple des cgroups ;
- les commandes utilisées.

---

# Challenge

Sans utiliser `docker inspect`, trouvez depuis l'hôte quel processus correspond à un conteneur donné.
