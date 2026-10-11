# Module 03 — Networking Docker

## Objectifs

Vous devez comprendre comment Docker connecte les conteneurs entre eux et avec l'extérieur.

---

# TP03 — Construire le réseau NovaCorp

## Partie A — Réseau par défaut

Lancez deux conteneurs sur le réseau Docker par défaut.

Identifiez :

- leurs adresses IP ;
- la gateway ;
- le bridge Linux associé ;
- les interfaces `veth`.

Depuis l'hôte, observez :

```text
docker0
interfaces veth
routes
```

---

## Partie B — Réseau utilisateur

Créez un réseau nommé :

```text
novacorp-backend
```

Connectez deux conteneurs.

Testez la communication :

- par IP ;
- par nom de conteneur.

Expliquez ce qui change par rapport au bridge par défaut.

---

## Partie C — Architecture à deux réseaux

Vous devez obtenir :

```text
            frontend
Client ----------------> nginx
                           |
                           |
                           v
                          api
                           |
                           |
                        backend
                           |
                           v
                        database
```

Contraintes :

- nginx doit être connecté au réseau frontend ;
- api doit pouvoir communiquer avec nginx et database ;
- database ne doit pas être directement accessible depuis le réseau frontend ;
- le port PostgreSQL ne doit pas être publié sur l'hôte.

---

## Partie D — Publication de ports

Expliquez la différence entre :

```text
EXPOSE 8000
```

et :

```text
-p 8000:8000
```

Testez différents bindings.

---

## Partie E — Diagnostic

Vous devez être capables d'utiliser :

```bash
docker network ls
docker network inspect
ip addr
ip route
ss -lntp
```

Ajoutez au moins deux autres commandes utiles.

---

# Livrable

Créez `networking.md` contenant :

- un schéma de l'architecture ;
- les réseaux créés ;
- les IP observées ;
- les commandes de diagnostic ;
- une explication du DNS interne Docker.

---

# Challenge

Retrouvez depuis Linux les interfaces `veth` correspondant à deux conteneurs précis.
