# Module 06 — Sécurité des conteneurs

## Contexte

La stack NovaCorp fonctionne.

Elle doit maintenant être sécurisée avant mise en production.

---

# TP06 — Audit et hardening

## Partie A — Audit

Analysez vos conteneurs.

Recherchez au minimum :

- utilisateur root ;
- ports inutiles ;
- secrets exposés ;
- capabilities inutiles ;
- conteneurs privilégiés ;
- accès au Docker socket ;
- images trop anciennes ;
- absence de limites de ressources ;
- filesystem modifiable inutilement.

---

## Partie B — Utilisateur non-root

Vérifiez quel utilisateur exécute votre application.

Modifiez votre image si nécessaire.

Validez avec :

```bash
id
```

depuis le conteneur.

---

## Partie C — Secrets

Recherchez les variables sensibles dans :

```bash
docker inspect
docker compose config
```

Expliquez les risques.

Proposez une méthode plus sûre que l'écriture d'un mot de passe directement dans le fichier Compose.

---

## Partie D — Capabilities

Recherchez :

```text
Linux capabilities Docker
```

Expliquez l'intérêt de :

```text
cap_drop
cap_add
```

Testez une réduction des capabilities sur au moins un service.

---

## Partie E — Filesystem

Essayez de rendre un conteneur :

```text
read_only
```

Identifiez les répertoires qui doivent éventuellement rester écrits.

---

## Partie F — Ressources

Appliquez des limites de :

- mémoire ;
- CPU.

Provoquez volontairement une consommation importante afin d'observer le comportement.

---

## Partie G — Scan d'image

Installez ou utilisez un scanner de vulnérabilités d'images comme :

```text
Trivy
```

Scannez au moins une de vos images.

Analysez les résultats.

Il n'est pas demandé de supprimer toutes les CVE.

Vous devez distinguer :

- présence d'une vulnérabilité ;
- exploitabilité ;
- sévérité ;
- correctif disponible.

---

# Livrable

Créez :

```text
security-audit.md
```

avec :

| Risque | Sévérité | Correction | Statut |
|---|---|---|---|

Vous devez identifier au minimum **8 points**.

---

# Challenge

Expliquez pourquoi monter :

```text
/var/run/docker.sock
```

dans un conteneur peut permettre une compromission complète de l'hôte.
