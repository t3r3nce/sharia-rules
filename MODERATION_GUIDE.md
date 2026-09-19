# Guide de Modération - Serveur Minecraft Sharia

Document interne pour l'équipe administrative du serveur Minecraft Sharia. Ce guide fournit les procédures et templates standardisés pour l'application du règlement.

---

## 📋 Table des Matières

1. [Procédures Générales](#procédures-générales)
2. [Gestion des Infractions](#gestion-des-infractions)
3. [Templates de Messages](#templates-de-messages)
4. [Escalade des Sanctions](#escalade-des-sanctions)
5. [Logs et Documentation](#logs-et-documentation)

---

## Procédures Générales

### Principes Fondamentaux
- **Impartialité :** Traiter tous les joueurs équitablement selon les règles
- **Documentation :** Enregistrer toutes les actions modératives
- **Transparence :** Communiquer clairement les raisons des sanctions
- **Rapidité :** Agir rapidement sur les violations évidentes
- **Proportionnalité :** Adapter la sanction à la gravité de l'infraction

### Avant de Sanctionner
1. Vérifier les logs serveur pour confirmer la violation
2. Examiner l'historique disciplinaire du joueur
3. Considérer les circonstances atténuantes (équivoque possible, première offense)
4. Consulter d'autres admins pour les cas complexes

### Après la Sanction
1. Documenter la violation dans les logs internes
2. Noter la date, l'heure et la raison exacte
3. Enregistrer le pseudo du joueur et son UUID
4. Conserver les screenshots/vidéos si disponibles

---

## Gestion des Infractions

### Niveau 1 : Avertissement
**Utilisé pour :** Premières violations mineures, comportement limite

| Infraction | Condition | Action |
|-----------|-----------|--------|
| Spam chat modéré | 3-5 messages flood | Message privé + warning public |
| Trash talk excessif | Insults légères, pas personnelles | Avertissement public |
| Ignorance du règlement | Nouveau joueur (< 1h) | Redirection vers règlement |

**Action :** Message direct au joueur en privé. Pas de sanction enregistrée.

---

### Niveau 2 : Mute (Restriction Chat)
**Utilisé pour :** Violations modérées de communication

| Infraction | Durée Recommandée |
|-----------|------------------|
| Spam chat | 30 minutes à 2 heures |
| Publicité | 1 heure à 24 heures |
| Insultes personnelles | 2-12 heures |
| Contenu toxique | 12-48 heures |

**Commande :** `/mute [pseudo] [durée]`

---

### Niveau 3 : Kick
**Utilisé pour :** Violation claire pendant la session

| Infraction | Urgence |
|-----------|---------|
| Comportement abusif continu | Immédiat |
| Tentative de hack/exploit | Immédiat |
| Contenu hate/discrimination | Immédiat |

**Commande :** `/kick [pseudo] [raison]`

---

### Niveau 4 : Ban Temporaire
**Utilisé pour :** Infractions graves ou récidive

| Infraction | Durée 1ère | Durée Récidive | Durée 3ème |
|-----------|-----------|----------------|-----------|
| Quit en combat | 3 jours | 7 jours | Permanent |
| Auto-clic PVP | 7 jours | 14 jours | Permanent |
| Fly hack | 14 jours | 30 jours | Permanent |
| X-Ray | Permanent | N/A | N/A |
| Toxicité grave | 7 jours | 14 jours | Permanent |

**Commande :** `/tempban [pseudo] [durée] [raison]`

---

### Niveau 5 : Ban Permanent
**Utilisé pour :** Infractions irréversibles

| Infraction | Raison |
|-----------|--------|
| X-Ray | Avantage unfair permanent |
| Fly/Speed hack établi | Compromet l'intégrité du jeu |
| RWT (Real World Trading) | Contrevient aux conditions Mojang |
| Harcèlement/discrimination grave | Violation de communauté |
| Ban tempban + récidive rapide | Pattern de misbehavior |

**Commande :** `/ban [pseudo] [raison]`

**Important :** Aucun appel n'est accepté pour les bans permanents.

---

### Niveau 6 : Confiscation d'Items
**Utilisé pour :** Quit en combat, vol dans contexte sanctionnable

**Procédure :**
1. Localiser l'inventaire du joueur
2. Noter tous les items précieux
3. Supprimer l'inventaire OU le transférer à la victime
4. Documenter l'action

**Commande :** `/clear [pseudo]` (ou transfert manuel via `/give`)

---

### Niveau 7 : Rollback/Destruction de Structures
**Utilisé pour :** Constructions problématiques (lag, griefing excessif automatisé)

**Conditions :**
- Lag serveur directement attributable
- Griefing à grande échelle automatisé
- Structures exploitant bugs serveur
- **Farms à lag** (Article 2.5)

**Procédure pour Farms à Lag :**
1. Vérifier les TPS actuels avec `/tps`
2. Identifier la farm problématique (F3 chunk debug)
3. Confirmer l'impact avec au moins un autre admin
4. **Aucun avertissement requis** - suppression directe autorisée
5. Notifier le joueur : "Votre farm a été supprimée pour cause de lag excessif."
6. Documenter dans les logs

**Types de Farms à Risque :**
- Farms avec 1000+ entités concentrées
- Redstone en boucle permanente
- Charged creeper farms
- Mob grinders sans dispersal system
- Portails Nether surcharges
- Chunk loaders excessifs (>20 chunks simultanés)

**Exemple Notification :**
```
[Administration]
Votre structure aux coordonnées [X Y Z] a été supprimée.
Raison: Farm à lag - Impact serveur excessif (TPS affecté)
Règlement: Article 2.5
Aucune compensation ne sera fournie.
```

**Sanction Escalade :**
- 1ère suppression : Pas de ban
- Récidive (même joueur reconstruction) : Avertissement + ban 3 jours
- 3ème : Ban permanent

---

## Templates de Messages

### Template 1 : Avertissement en Privé
```
[Modérateur] Hello [Pseudo],

On a remarqué que tu spam un peu trop dans le chat. Veille à respecter 
les règles de communication (Article 6.2).

C'est juste un avertissement amical. Pas de problème si tu arrêtes là !

Règlement : https://sharia-rules.github.io

Merci de ta compréhension.
```

### Template 2 : Notification de Mute
```
[Modérateur] [Pseudo] a reçu un mute pour 2 heures.
Raison: Spam chat / Publicité serveur externe

Rappel: Article 6.2 du règlement. https://sharia-rules.github.io
```

### Template 3 : Notification de Kick
```
Tu as été éjecté du serveur.

Raison: Langage toxique et insultes personnelles graves

Règlement: Article 6.1-6.2
https://sharia-rules.github.io

Attente de 24h avant reconnexion.
```

### Template 4 : Notification de Ban Temporaire
```
Tu as été banni temporairement pour 7 JOURS.

Raison: Auto-clic pendant combat PVP

Infraction: Article 2.2 - Limite auto-clic farming uniquement
Précédent: Première violation

Règlement: https://sharia-rules.github.io

Date de débannissement: [DATE+7JOURS]
```

### Template 5 : Notification de Ban Permanent
```
Tu as été banni DÉFINITIVEMENT du serveur.

Raison: X-Ray (Vision traversant les blocs)

Infraction: Article 5.1 - X-Ray strictement interdit

Règlement: https://sharia-rules.github.io

DÉCISION DÉFINITIVE - AUCUN APPEL N'EST ACCEPTÉ.
```

### Template 6 : Avertissement Publique (Chat)
```
[Administration] 
⚠️ Rappel important: Ne spam pas dans le chat.
Consultez le règlement: https://sharia-rules.github.io

Prochaine violation = Mute automatique.
```

---

## Escalade des Sanctions

### Récidive : Processus Standard
```
1ère Offense  → Avertissement/Mute court (2h)
2ème Offense  → Mute plus long (24h)
3ème Offense  → Kick + Mute 48h
4ème Offense  → Ban temporaire 7 jours
5ème+         → Ban permanent
```

### Infraction Grave : Bypass
Certaines infractions justifient un bypass direct de cette gradation :
- X-Ray → Ban permanent directement
- RWT → Ban permanent directement
- Harcèlement grave → Ban permanent directement
- Toxicité majeure (hate/discrimination) → Ban direct permanent

---

## Documentation & Logs

### Format de Log Recommandé
```
[DATE] [HEURE] [PSEUDO] [RAISON] [SANCTION] [DURÉE] [NOTES]

Exemple:
2026-09-15 14:32 PlayerName X-Ray Detection BAN_PERMANENT N/A UUID:xxxx... | Logs confirm sight through stone blocks
2026-09-15 15:15 PlayerName Quit in Combat BAN_TEMP 7d UUID:yyyy... | Player quit 5 seconds after combat engagement
2026-09-15 16:00 PlayerName Spam MUTE 2h UUID:zzzz... | 4 consecutive messages, first offense
```

### Éléments à Enregistrer
- Pseudo du joueur
- UUID unique
- Date et heure exacte
- Infraction spécifique (article du règlement)
- Sanction appliquée
- Durée (si applicable)
- Raison détaillée
- Screenshots/preuves (liens ou descriptions)
- Admin responsable

### Accès aux Logs
- Fichier central: `/logs/moderation.txt` (serveur)
- Google Sheet sécurisé pour suivi moyen/long terme
- Backup mensuel des logs critiques

---

## Procédures Spéciales

### Dealing with Appeals (Gestion des Appels)
Le règlement stipule: **Aucun appel n'est accepté.**

**Procédure:**
1. Recevoir le message d'appel
2. Répondre: "Les décisions administratives sont définitives et ne sont pas sujettes à appel."
3. Ne pas relancer de discussion
4. Archiver l'appel dans les logs

### Cas de Doute
Si vous douter de la culpabilité:
1. Demander confirmation à un autre admin
2. Consulter les logs multiples
3. Attendre une deuxième infraction avant sanction (sauf X-Ray/fly)
4. Documenter le doute dans les notes

### Admins Problématiques
Si un admin abuse de ses pouvoirs:
1. Alerter le chef admin / propriétaire du serveur
2. Documenter les abus (logs, screenshots)
3. Procédure de révocation ad-hoc
4. Jamais de confrontation publique

---

## Checklist Quotidienne du Modérateur

- [ ] Vérifier les logs serveur (crashes, bugs)
- [ ] Lire le chat global pour toxicité/spam
- [ ] Vérifier les bans expirant (débannissement)
- [ ] Examiner les rapports de joueurs
- [ ] Mettre à jour le document de sanctions
- [ ] Backuper les logs critiques
- [ ] Communiquer avec l'équipe admin (Discord)

---

## Contact & Escalade

**Hiérarchie de Décision:**
1. Modérateur → Peut: Kick, Mute court, Avertissement
2. Modérateur Senior → Peut: Ban temporaire jusqu'à 7 jours
3. Admin → Peut: Ban permanent, Rollback structures
4. Chef Admin / Propriétaire → Décisions finales sur appels

**En cas de problème:**
- Discord interne: #moderation
- Email admin: [email]
- Réunion hebdomadaire: [jour/heure]

---

**Dernière mise à jour:** Septembre 2026  
**Version:** 1.0  
**Auteur:** Administration Sharia  

**Rappel:** Ce guide est interne. Ne pas partager avec les joueurs.
