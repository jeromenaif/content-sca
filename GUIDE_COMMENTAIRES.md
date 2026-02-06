# 🚀 Configuration Commentaires - Scarlet Mars 2026 Generator

## ✅ Ce qui a été ajouté

Votre générateur visuel a maintenant une **section commentaires** sous chaque publication qui permet à votre collègue graphiste de laisser des feedbacks directement sur chaque post.

### Nouvelles fonctionnalités :
- 💬 Section commentaires dynamique qui change selon le post sélectionné
- 📝 Guide de feedback intégré
- 🔔 Notifications email automatiques
- 🎨 Design cohérent avec votre interface existante
- 🌙 Thème dark adapté à votre charte graphique

---

## ⚙️ Configuration en 3 étapes

### Étape 1 : Activer GitHub Discussions

1. Sur votre repo `jeromenaif/content-sca`, allez dans **Settings**
2. Scrollez jusqu'à **Features**
3. Cochez ✅ **Discussions**
4. Cliquez sur **Discussions** (nouvel onglet)
5. Créez une catégorie :
   - **Nom** : `Publications`
   - **Description** : "Feedback sur les publications Scarlet"
   - **Format** : "Open-ended discussion"

### Étape 2 : Obtenir vos IDs giscus

1. Allez sur **https://giscus.app/**
2. Configurez :
   ```
   Repository : jeromenaif/content-sca
   Discussion Category : Publications
   Mapping : specific term
   ```
3. **Copiez ces 2 valeurs** du script généré :
   ```html
   data-repo-id="R_kgD..."           ← Copiez cette valeur
   data-category-id="DIC_kwD..."     ← Copiez cette valeur
   ```

### Étape 3 : Mettre à jour le HTML

1. Ouvrez `Scarlet_Mars2026_Generator_v2_with_comments.html`
2. Cherchez (ligne ~512) :
   ```javascript
   script.setAttribute('data-repo-id', 'VOTRE_REPO_ID'); 
   script.setAttribute('data-category-id', 'VOTRE_CATEGORY_ID');
   ```
3. Remplacez par vos vraies valeurs :
   ```javascript
   script.setAttribute('data-repo-id', 'R_kgD...');
   script.setAttribute('data-category-id', 'DIC_kwD...');
   ```
4. Sauvegardez

---

## 🎯 Comment ça fonctionne

### Système intelligent de commentaires par post

Chaque publication (Post #1, #2, #3, etc.) a ses **propres commentaires séparés** :

- **Post #1** → Discussion "Publication-1-Mars-2026"
- **Post #2** → Discussion "Publication-2-Mars-2026"
- **Post #3** → Discussion "Publication-3-Mars-2026"
- etc.

Quand votre collègue change de post dans le sélecteur, la section commentaires se recharge automatiquement avec les bons commentaires !

---

## 📤 Déploiement

### Option A : GitHub Pages (Recommandé)

```bash
# 1. Renommez le fichier
mv Scarlet_Mars2026_Generator_v2_with_comments.html index.html

# 2. Push vers GitHub
git add index.html
git commit -m "Ajout système de commentaires giscus"
git push

# 3. Activez GitHub Pages dans Settings → Pages
# Source : main branch, / (root)

# 4. Votre site sera sur :
# https://jeromenaif.github.io/content-sca/
```

### Option B : Usage local

1. Ouvrez simplement le fichier HTML dans votre navigateur
2. Partagez-le via Google Drive / Dropbox
3. Les commentaires fonctionneront quand même !

---

## 💬 Workflow collaboratif

### Pour vous (Jérôme) :
1. Ouvrez le HTML dans votre navigateur
2. Changez de post avec le sélecteur
3. Scrollez pour voir les commentaires
4. Recevez des notifications email à chaque feedback

### Pour votre collègue graphiste :
1. Ouvre le lien que vous lui envoyez
2. Parcourt les posts un par un
3. Laisse des commentaires :
   - ✅ "Validé pour moi"
   - 🎨 "Peut-on agrandir le titre ?"
   - ✍️ "Typo à corriger : 'nothre' → 'notre'"
4. Peut réagir avec des emojis : 👍 ❤️ 🎉

---

## 🎨 Personnalisation (optionnel)

### Changer le thème des commentaires

Dans le fichier, ligne ~522, vous pouvez changer :
```javascript
script.setAttribute('data-theme', 'dark');  // Options : light, dark, preferred_color_scheme
```

### Changer la langue

```javascript
script.setAttribute('data-lang', 'fr');  // Options : fr, nl, en
```

---

## 🔔 Notifications

### Activer les emails :
1. Sur GitHub : **Settings** → **Notifications**
2. Cochez **Discussions**
3. Vous recevrez un email à chaque nouveau commentaire

---

## ✨ Avantages

✅ Aucun backend à gérer
✅ Gratuit et open-source
✅ Notifications automatiques
✅ Historique complet dans GitHub Discussions
✅ Système de réactions (👍 ❤️ 🎉)
✅ Markdown supporté dans les commentaires
✅ Commentaires séparés par post

---

## 🆘 Problèmes fréquents

### giscus ne s'affiche pas
- ✓ Vérifiez que Discussions est activé
- ✓ Vérifiez les IDs data-repo-id et data-category-id
- ✓ Le repo doit être **public** pour giscus

### Les commentaires ne se rechargent pas entre les posts
- ✓ Videz le cache du navigateur (Ctrl+Shift+R)
- ✓ Vérifiez la console JavaScript (F12)

### Ma collègue ne peut pas commenter
- ✓ Elle doit avoir un compte GitHub (gratuit)
- ✓ Elle doit s'authentifier la première fois

---

## 📞 Support

Questions ? → @jeromenaif sur GitHub

---

**Made with ❤️ for Scarlet Content Factory**
