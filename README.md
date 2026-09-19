# Règlement Serveur Minecraft - Sharia

Dépôt officiel contenant le règlement complet du serveur Minecraft **Sharia**. Ce document définit les règles, restrictions et sanctions applicables à tous les joueurs.

## 📋 Contenu du Règlement

Le règlement est organisé en **7 sections majeures** :

### I. Dispositions Générales et Principes Fondamentaux
- Acceptation obligatoire du règlement
- Autorité absolue de l'administration
- Absence de recours aux décisions administratives
- Responsabilité des joueurs

### II. Gameplay & Mécaniques de Jeu
- Statut légal de l'AFK (autorisé sans compensation)
- Auto-clic autorisé exclusivement pour le farming
- Mods de schématiques et construction automatique (autorisés)
- Alliances illimitées entre joueurs
- Gestion de la performance serveur

### III. PVP, Combat et Pillage
- PVP autorisé sans restriction
- Pillage et destruction complètement autorisés
- **Quitter en combat (+ 30s après) = infraction majeure** (confiscation d'items)
- Aucun droit de propriété garanti

### IV. Construction, Propriété et Griefing
- Griefing totalement autorisé
- Vol dans les chests sans restriction
- Aucune zone protégée
- Pas de compensation en cas de griefing

### V. Modifications, Hacks et Exploits Interdits
- X-Ray → Ban permanent
- Fly/Teleport hack → Ban
- Cheats donnant avantage → Ban
- Clients modifiés (Lunar, Badlion) autorisés si conformes
- Exploits vanilla soumis à discrétion admin

### VI. Conduite et Communication
- Respect humain minimum requis (trash talk autorisé)
- Contenu toxique interdit (haine, menaces, spam)
- Pas d'impersonation admin
- Pas de transactions argent réel
- Pas de publicité d'autres serveurs

### VII. Système de Sanctions et Modération
- Avertissement → Mute → Kick → Ban temporaire → Ban permanent
- Confiscation d'items en cas de violation
- Aucun appel des décisions
- Admin peut dévier des protocoles si nécessaire

---

## 🌐 Accès au Règlement

### Version Web
- **Site officiel :** https://t3r3nce.github.io/sharia-rules/
- **Lien direct :** Ouvrez dans votre navigateur

### Fonctionnalités du Site
- **🔍 Barre de recherche avancée** : Entrez des mots-clés pour trouver rapidement les articles
  - Exemples: "X-Ray", "AFK", "Combat", "Quit", "Farm", "Lag", "VPN", "TP", "Inspection"
  - Recherche en temps réel avec highlighting des résultats
  - Affichage du nombre de résultats trouvés
- **📌 Navigation sticky** : Accès facile aux sections depuis n'importe où
- **📱 Responsive design** : Fonctionne sur mobile, tablette et desktop
- **⚡ Filtre dynamique** : Les sections vides sont automatiquement masquées lors d'une recherche

### En Jeu
Partagez le lien Discord ou créez un panneau avec la commande `/rules` (plugin EssentialsX recommandé).

---

## 🚀 Déploiement sur GitHub Pages

### Étape 1 : Créer un dépôt GitHub
```bash
# Cloner ce dépôt (ou créer un nouveau)
git clone https://github.com/[votre-username]/sharia-rules.git
cd sharia-rules
```

### Étape 2 : Placer les fichiers
```
sharia-rules/
├── index.html          # Page principale du règlement
├── README.md          # Ce fichier
└── .gitignore         # (Optionnel)
```

### Étape 3 : Pousser vers GitHub
```bash
git add .
git commit -m "Initial commit: Règlement serveur Sharia"
git push origin main
```

### Étape 4 : Activer GitHub Pages
1. Allez sur **Settings** → **Pages**
2. Sélectionnez **Deploy from a branch**
3. Branche : **main**, dossier : **/ (root)**
4. Cliquez sur **Save**

Votre site sera accessible à : `https://[votre-username].github.io/sharia-rules/`

---

## 📝 Modification du Règlement

### Ajouter/Modifier une règle
1. Modifiez le fichier `index.html`
2. Localisez la section pertinente (id: `#general`, `#gameplay`, etc.)
3. Ajoutez ou modifiez un élément `.rule`

### Format d'une règle
```html
<div class="rule">
    <h3>Article X.X - Titre de la Règle</h3>
    <p>Description de la règle...</p>
    <div class="subsection">
        <strong>Sous-titre :</strong> Détails additionnels.
    </div>
</div>
```

### Pousser les modifications
```bash
git add index.html
git commit -m "Mise à jour: [description du changement]"
git push origin main
```

Les changements seront visibles en ligne en quelques secondes (cache GitHub).

---

## 🎨 Personnalisation du Design

### Couleurs principales
Les variables CSS dans `index.html` peuvent être modifiées :

```css
:root {
    --primary: #1a1a1a;           /* Fond sombre */
    --accent: #c41e3a;            /* Couleur accentuée (rouge) */
    --text: #e8e8e8;              /* Texte clair */
    --text-muted: #a8a8a8;        /* Texte grisé */
    --border: #404040;            /* Bordures */
    --highlight: #3d3d3d;         /* Fond des règles */
}
```

Modifiez les valeurs hexadécimales pour adapter au style de votre serveur.

---

## 📖 Clauses Principales

### Acceptation Obligatoire
> Toute personne se connectant au serveur accepte explicitement et sans réserve l'intégralité du présent règlement.

### Autorité Administrative
> Les administrateurs du serveur se réservent le droit unilatéral de sanctionner tout utilisateur s'ils estiment que la preuve de la violation est suffisante.

### Absence de Recours
> Les décisions de l'administration ne sont pas sujettes à appel ou révision par les joueurs.

---

## ⚠️ Infractions Graves (Ban Direct)

- ❌ X-Ray
- ❌ Fly hack / Speed hack
- ❌ Aimbots / Combat enhancements
- ❌ Quitter en combat (répété)
- ❌ Transactions argent réel
- ❌ Contenu de haine/discrimination

---

## ✅ Autorisé

- ✓ PVP sans limite
- ✓ Griefing complet
- ✓ Auto-clic pour farming
- ✓ Schématiques de structures
- ✓ Alliances illimitées (même 5v1)
- ✓ AFK sans compensation
- ✓ Clients modifiés (conformes)
- ✓ VPN autorisé
- ✓ Comptes secondaires/alts illimités
- ✓ Comptes simultanés autorisés
- ✓ Partage d'IP (frères, sœurs, colocataires)
- ✓ Échanges entre joueurs (trading)
- ✓ TP Kill avec 5s de grâce post-TP

---

## 📞 Contact & Support

- **Discord :** [Lien vers votre serveur Discord]
- **Email :** [Adresse administrative]
- **Site Principal :** [URL du serveur]

---

## 📜 Version & Historique

| Version | Date | Changements |
|---------|------|-------------|
| 1.0 | Septembre 2026 | Version initiale du règlement |

---

## 📄 Licence

Ce règlement s'applique exclusivement au serveur Minecraft **Sharia**. La copie, reproduction ou utilisation de ce document pour d'autres serveurs sans permission est interdite.

---

**Dernière mise à jour :** Septembre 2026

**Serveur Minecraft - Sharia**
