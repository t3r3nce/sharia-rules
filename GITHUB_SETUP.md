# Guide: Répondre à la Question .gitignore sur GitHub

## La Question de GitHub

Quand vous créez un nouveau dépôt, GitHub vous demande :

> "Add a .gitignore? Choose a template..."

---

## 🎯 Réponse Recommandée pour "Sharia Rules"

### **Catégorie à Sélectionner:** `None`

**Pourquoi ?**

Votre projet est un **site web statique HTML/CSS/JavaScript** pour GitHub Pages. C'est un dépôt très simple sans dépendances complexes.

Les templates de .gitignore proposés par GitHub sont généralement pour :
- `Node` (npm/Node.js) → Vous n'avez pas besoin
- `Python` → Vous n'avez pas besoin
- `Java` → Vous n'avez pas besoin

**Solution:**
1. Sélectionnez **"None"** (aucun template)
2. Vous avez déjà un `.gitignore` custom que vous allez ajouter manuellement

---

## ✅ Alternative: Ce Que Vous Pourriez Faire

### Option 1: Créer le dépôt SANS .gitignore (RECOMMANDÉ)
```bash
# Sur GitHub
# Create repository → Skip .gitignore
# Cloner et ajouter les fichiers
git clone https://github.com/[votre-username]/sharia-rules.git
cd sharia-rules

# Copier les fichiers fournis (index.html, README.md, etc.)
# Copier aussi le .gitignore custom

git add .
git commit -m "Initial: Règlement serveur Sharia avec .gitignore"
git push origin main
```

### Option 2: Créer avec .gitignore GitHub (Puis Remplacer)
```bash
# Sur GitHub
# Create repository → Sélectionner template
# Cloner
git clone https://github.com/[votre-username]/sharia-rules.git
cd sharia-rules

# PUIS remplacer le .gitignore par le vôtre
# Copier le .gitignore fourni par-dessus

git add .gitignore
git commit -m "Update: Utiliser .gitignore personnalisé"
git push origin main
```

---

## 📋 Contenu du .gitignore pour Votre Projet

Le fichier `.gitignore` fourni ignore :

```
# Système d'exploitation
.DS_Store
Thumbs.db

# Éditeurs & IDE
.vscode/
.idea/
*.swp

# Fichiers temporaires
*.tmp
.cache/
temp/

# Node (si vous ajoutez npm à l'avenir)
node_modules/
package-lock.json

# Environnement
.env
.env.local
```

**Aucune chance de "committé" accidentellement des fichiers inutiles !**

---

## 🚀 Résumé Rapide

| Étape | Action |
|-------|--------|
| 1 | Créer dépôt sur GitHub → `.gitignore: None` |
| 2 | Cloner le dépôt |
| 3 | Ajouter tous les fichiers fournis |
| 4 | `git add . && git commit && git push` |
| 5 | Configurer GitHub Pages (Settings → Pages) |
| 6 | Accéder au site : `https://[username].github.io/sharia-rules/` |

---

**Vous êtes maintenant prêt à déployer ! 🎮**
