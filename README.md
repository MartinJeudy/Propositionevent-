# Hormur - Nouveau parcours Propositions d'événements

## 🎯 Description

Prototype interactif du nouveau parcours utilisateur pour les propositions d'événements sur la plateforme Hormur.

### Fonctionnalités

✅ **Vue responsive** - Optimisé pour mobile (+70% des utilisateurs) et desktop  
✅ **2 actions principales** - "Refuser" ou "Accepter"  
✅ **Modale post-acceptation** - Choix entre "Discuter de la date" ou "Créer l'événement"  
✅ **Design Hormur** - Couleurs et style cohérents avec la marque  
✅ **Animations fluides** - Transitions douces et feedback visuel  

## 🚀 Déploiement sur Netlify

### Option 1 : Drag & Drop (Plus simple)

1. Allez sur [https://app.netlify.com/drop](https://app.netlify.com/drop)
2. Glissez-déposez le dossier `hormur-propositions` complet
3. Netlify va déployer automatiquement
4. Vous recevrez une URL de type `https://random-name.netlify.app`

### Option 2 : Via Git (Recommandé)

1. Créez un nouveau repository GitHub
2. Poussez ce code sur le repository :
```bash
git init
git add .
git commit -m "Initial commit - Hormur propositions prototype"
git remote add origin YOUR_REPO_URL
git push -u origin main
```

3. Sur Netlify :
   - Cliquez sur "Add new site" → "Import an existing project"
   - Connectez votre repository GitHub
   - Build settings : laissez vide (site statique)
   - Publish directory : laissez vide ou mettez `.`
   - Cliquez sur "Deploy site"

### Option 3 : Netlify CLI

```bash
npm install -g netlify-cli
cd hormur-propositions
netlify deploy --prod
```

## 📱 Test en local

Ouvrez simplement le fichier `index.html` dans votre navigateur :
- Double-cliquez sur le fichier
- Ou utilisez un serveur local : `python -m http.server 8000`

## 🎨 Personnalisation

### Modifier les couleurs Hormur

Dans le fichier `index.html`, cherchez :
```css
.btn-primary {
    background: linear-gradient(135deg, #FF6B4A 0%, #FF8C6A 100%);
}
```

Modifiez `#FF6B4A` et `#FF8C6A` avec vos couleurs exactes.

### Modifier les données de test

Dans le fichier `index.html`, cherchez l'objet `proposalData` :
```javascript
const proposalData = {
    artist: {
        name: "Durand avec un d",
        // ... modifiez ici
    },
    event: {
        venue: "Chez vous",
        // ... modifiez ici
    }
};
```

## 📋 Structure du projet

```
hormur-propositions/
├── index.html          # Application complète (React + CSS + JS)
└── README.md          # Ce fichier
```

## 🔧 Technologies utilisées

- **React 18** - Framework UI
- **Tailwind CSS** - Styling utility-first
- **Babel Standalone** - Transpilation JSX dans le navigateur

## 📸 Captures d'écran

### Vue Mobile
- Page de proposition avec 2 boutons
- Modale post-acceptation avec 2 options

### Vue Desktop
- Layout 3 colonnes
- Zone d'action dédiée à droite

## 🎯 Parcours utilisateur

1. **Réception de la proposition** → L'hôte visualise les détails
2. **Décision** → Refuser ou Accepter
3. **Si Acceptation** → Modale avec 2 choix :
   - **Discuter** → Ouvre la messagerie
   - **Créer** → Crée l'événement immédiatement

## ⚡ Prochaines étapes

- [ ] Intégration avec l'API Hormur réelle
- [ ] Connexion à la base de données
- [ ] Système de messagerie en temps réel
- [ ] Tests utilisateurs
- [ ] Tracking analytics

## 📞 Support

Pour toute question : martin@hormur.com

---

**Hormur** - L'art où on ne l'attend pas 🎨
