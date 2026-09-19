# Guide de Déploiement - Serveur Sharia Règlement

Votre site est déjà en ligne à : **https://t3r3nce.github.io/sharia-rules/**

## ✅ Configuration GitHub Pages

Votre GitHub Pages est automatiquement configuré pour afficher le contenu du dépôt.

### Vérifier la Configuration

1. Allez sur GitHub → Settings (Paramètres)
2. Cherchez **Pages** (à gauche, dans le menu)
3. Vérifiez que :
   - **Source** est défini sur "Deploy from a branch"
   - **Branch** est "main" (ou "master")
   - **Folder** est "/" (racine)
   - **Enforce HTTPS** est activé ✓

### Si le site ne fonctionne pas

1. Vérifiez que le fichier `index.html` est à la racine (pas dans un dossier)
2. Attendez 1-2 minutes après un push (GitHub Pages prend du temps à se mettre à jour)
3. Vérifiez qu'il n'y a pas d'erreur dans les logs (Settings → Pages → Show details)

---

## 🚀 Mise à Jour du Site

### Éditer une Règle Existante

1. **Cloner le dépôt** (si pas déjà fait) :
```bash
git clone https://github.com/t3r3nce/sharia-rules.git
cd sharia-rules
```

2. **Éditer le fichier** `index.html` avec votre éditeur (VS Code, Sublime, etc.)

3. **Chercher la section à modifier** :
   - Utilisez Ctrl+F pour chercher le titre de la règle
   - Ex: "Article 2.1" ou "AFK"

4. **Faire les changements** et sauvegarder

5. **Pousser vers GitHub** :
```bash
git add index.html
git commit -m "Mise à jour: Modification de l'Article X.X"
git push origin main
```

6. **Vérifier le changement** :
   - Attendez 30-60 secondes
   - Actualisez https://t3r3nce.github.io/sharia-rules/ (Ctrl+Shift+R pour vider le cache)

### Ajouter une Nouvelle Règle

1. Ouvrir `index.html`
2. Chercher la section appropriée (ex: `<section id="gameplay">`)
3. Ajouter avant la fermeture `</section>` :

```html
<div class="rule">
    <h3>Article X.X - Titre de la Nouvelle Règle</h3>
    <p>Description de la règle...</p>
    <div class="subsection">
        <strong>Détail :</strong> Information supplémentaire.
    </div>
</div>
```

4. Sauvegarder et pousser vers GitHub

---

## 🔍 Tester la Barre de Recherche

### Sur le site en ligne :
1. Ouvrez https://t3r3nce.github.io/sharia-rules/
2. Cherchez la **barre de recherche** sous le menu de navigation
3. Tapez des mots-clés pour tester :
   - `X-Ray` → Trouve Article 5.1
   - `AFK` → Trouve Article 2.1
   - `VPN` → Trouve Article 1.6
   - `TP` → Trouve Article 3.6
   - `Inspection` → Trouve Article 1.7
   - `Farm` → Trouve Article 2.5

### Si la recherche ne fonctionne pas :
1. Ouvrez les outils développeur (F12 ou Ctrl+Shift+I)
2. Allez dans l'onglet "Console"
3. Vérifiez qu'il n'y a pas d'erreurs en rouge
4. Si erreur: signallez le problème

---

## 📋 Structure des Fichiers

```
sharia-rules/
├── index.html              ← Site web complet (à modifier)
├── README.md               ← Documentation principale
├── FAQ.md                  ← Questions fréquentes
├── MODERATION_GUIDE.md     ← Guide admin (interne)
├── GITHUB_SETUP.md         ← Guide setup initial
├── DEPLOY.md               ← Ce fichier
├── _config.yml             ← Config GitHub Pages
├── .gitignore              ← Fichiers à ignorer
└── .git/                   ← Repository Git (auto)
```

---

## 🎯 Exemple : Ajouter une Nouvelle Règle

### Scénario: Vous voulez ajouter une règle sur les "Nuke" de serveur

**Étape 1:** Éditer `index.html`, trouver section appropriée
```html
<section id="modifications">
    <h2>V. Modifications, Hacks et Exploits Interdits</h2>
    
    <!-- Ajouter après Article 5.5 -->
    <div class="rule">
        <h3>Article 5.6 - Nuke de Serveur et Destruction Massive</h3>
        <p>Utiliser des commandes admin ou exploits pour détruire massivement le serveur (nuke) est interdit et constitue une violation grave.</p>
        <div class="subsection">
            <strong>Exemples :</strong> Fill 1000x1000 blocs, suppression de biome entier, destruction de spawn.
        </div>
        <div class="subsection">
            <strong>Sanction :</strong> Ban permanent immédiat.
        </div>
    </div>
</section>
```

**Étape 2:** Sauvegarder et pousser
```bash
git add index.html
git commit -m "Ajout: Article 5.6 - Interdiction nuke de serveur"
git push origin main
```

**Étape 3:** Vérifier en ligne après 1 minute

---

## 💻 Outils Recommandés

### Éditer index.html
- **VS Code** (gratuit, très puissant) - https://code.visualstudio.com/
- **Sublime Text** (gratuit) - https://www.sublimetext.com/
- **Notepad++** (gratuit) - https://notepad-plus-plus.org/

### Éditer sur GitHub directement (simple)
1. Ouvrez https://github.com/t3r3nce/sharia-rules/
2. Cliquez sur `index.html`
3. Cliquez sur l'icône **"Modifier ce fichier"** (crayon en haut)
4. Faites vos changements
5. Cliquez **"Commit changes"** en bas
6. Écrivez un message et validez

---

## 🆘 Dépannage

### Le site n'apparaît pas à l'URL correcte
- Vérifiez que le dépôt est public (Settings → Public)
- Vérifiez le nom du dépôt (doit être `sharia-rules`)
- L'URL doit être: `https://t3r3nce.github.io/sharia-rules/`

### Les changements ne s'affichent pas
- Attendez 1-2 minutes
- Faites Ctrl+Shift+R (vider le cache du navigateur)
- Vérifiez que le push s'est bien fait (`git status` doit être "nothing to commit")

### La barre de recherche ne fonctionne pas
- Ouvrez la console (F12 → Console)
- Vérifiez qu'il n'y a pas d'erreurs JavaScript rouges
- Essayez dans un autre navigateur

### Les fichiers ne s'ajoutent pas
```bash
git status                    # Vérifier les changements
git add .                     # Ajouter tout
git commit -m "Message"       # Committer
git push origin main          # Pousser
```

---

## 📞 Support

Pour plus d'aide sur GitHub Pages :
- Documentation officielle: https://docs.github.com/en/pages
- Si problème technique: Cherchez sur Stack Overflow

Pour les changements du règlement:
- Contactez l'administration du serveur
- Créez un issue sur GitHub

---

**Serveur Sharia - Déploiement ✓**  
**Site en ligne:** https://t3r3nce.github.io/sharia-rules/  
**Dernière mise à jour:** Septembre 2026
