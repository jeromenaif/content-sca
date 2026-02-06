# 📝 Configuration Tally.so - Scarlet Mars 2026 Generator

## 🎯 Pourquoi Tally.so ?

✅ **Aucun compte requis** pour votre collègue
✅ Gratuit (jusqu'à 100 réponses/mois)
✅ Interface moderne et intuitive
✅ Notifications email automatiques
✅ Toutes les réponses dans un dashboard
✅ Export Excel/CSV possible

---

## 🚀 Configuration en 5 minutes

### Étape 1️⃣ : Créer un compte Tally.so

1. Allez sur **https://tally.so**
2. Cliquez sur **Sign up for free**
3. Créez votre compte (email + mot de passe)
4. Confirmez votre email

---

### Étape 2️⃣ : Créer le formulaire de feedback

1. Sur le dashboard Tally, cliquez sur **Create new form**
2. Choisissez **Start from scratch**
3. Donnez un nom : **"Scarlet Mars 2026 - Feedback Publications"**

---

### Étape 3️⃣ : Ajouter les champs du formulaire

Ajoutez ces champs dans l'ordre :

#### Champ 1 : Numéro de Publication (Hidden)
- Type : **Hidden field**
- Label : `post`
- Description : *Ce champ sera automatiquement rempli*

#### Champ 2 : Nom (Optionnel)
- Type : **Short text**
- Label : `Votre nom`
- Placeholder : `Ex: Marie`
- ⚙️ Settings : Décochez "Required" (optionnel)

#### Champ 3 : Statut de validation
- Type : **Multiple choice**
- Label : `Statut de cette publication`
- Options :
  - ✅ `Validé - OK pour publication`
  - ⏳ `En attente - Modifications demandées`
  - ❌ `À revoir complètement`

#### Champ 4 : Type de feedback
- Type : **Multiple choice** (autoriser plusieurs réponses)
- Label : `Type de commentaire` (optional)
- Options :
  - 🎨 `Modifications visuelles`
  - ✍️ `Corrections texte`
  - 💡 `Suggestions alternatives`
  - 📏 `Dimensions / Proportions`
  - 🎨 `Couleurs`

#### Champ 5 : Commentaire détaillé
- Type : **Long text**
- Label : `Votre commentaire`
- Placeholder : `Décrivez vos modifications, corrections ou suggestions...`
- ⚙️ Settings : Cochez "Required"
- Rows : 6

#### Champ 6 : Email (Optionnel)
- Type : **Email**
- Label : `Votre email (si vous souhaitez une réponse)`
- Placeholder : `votre@email.com`
- ⚙️ Settings : Décochez "Required"

---

### Étape 4️⃣ : Personnaliser l'apparence

1. Cliquez sur **Design** (icône palette en haut)
2. **Theme** : Dark (pour matcher votre interface)
3. **Primary color** : `#E61F13` (rouge Scarlet)
4. **Background** : Transparent
5. **Submit button text** : `Envoyer mon feedback`

---

### Étape 5️⃣ : Configurer les notifications

1. Cliquez sur **Settings** (icône engrenage)
2. Allez dans **Notifications**
3. Activez **Email notification**
4. Entrez votre email : `votre-email@exemple.com`
5. Message : `Nouveau feedback sur Publication #{{post}}`

---

### Étape 6️⃣ : Activer et obtenir l'URL d'intégration

1. En haut à droite, cliquez sur **Publish**
2. Le formulaire est maintenant actif ✅
3. Cliquez sur **Share** → **Embed on website**
4. Copiez le **Form ID** (c'est la partie après `/embed/`)

Exemple : 
```
https://tally.so/embed/wgbxQl
                           ^^^^^^
                        Form ID = wgbxQl
```

---

### Étape 7️⃣ : Intégrer dans le HTML

1. Ouvrez `Scarlet_Mars2026_Generator_v2_with_comments.html`
2. Trouvez la ligne (environ ligne 490) :
   ```javascript
   const tallyFormId = 'VOTRE_FORM_ID';
   ```
3. Remplacez par votre Form ID :
   ```javascript
   const tallyFormId = 'wgbxQl'; // Exemple
   ```
4. Sauvegardez ✅

---

## ✨ C'est fait ! Testez

1. Ouvrez le HTML dans votre navigateur
2. Sélectionnez un post (ex: Post #1)
3. Scrollez jusqu'à la section commentaires
4. Vous devriez voir le formulaire Tally intégré
5. Testez en laissant un commentaire

---

## 📧 Recevoir les réponses

### Dashboard Tally
1. Connectez-vous sur **https://tally.so**
2. Cliquez sur votre formulaire
3. Allez dans **Responses**
4. Vous voyez toutes les réponses en temps réel

### Notifications Email
Vous recevrez un email à chaque nouveau feedback avec :
- Le numéro de post concerné
- Le nom de la personne (si fourni)
- Le statut (Validé / En attente / À revoir)
- Le commentaire complet

### Export des données
1. Dans **Responses**, cliquez sur **Export**
2. Choisissez **Excel** ou **CSV**
3. Toutes vos réponses sont exportées

---

## 🎯 Workflow collaboratif

### Pour vous (Jérôme) :
1. Partagez le lien du générateur
2. Recevez des notifications par email
3. Consultez les feedbacks dans Tally.so
4. Exportez si besoin

### Pour votre collègue :
1. Ouvre le lien
2. Navigue entre les posts
3. Laisse un feedback **sans créer de compte**
4. Clique sur "Envoyer"
5. C'est tout ! ✨

---

## 💡 Astuces Pro

### Identifier facilement les posts
Le champ caché `post` contient automatiquement le numéro du post (1, 2, 3...).
Dans votre dashboard Tally, vous verrez :
```
Post: 1
Nom: Marie
Statut: Validé - OK pour publication
Commentaire: Super ! RAS
```

### Filtrer les réponses
Dans Tally, vous pouvez filtrer par :
- Numéro de post
- Statut (Validé / En attente / À revoir)
- Date de soumission

### Partager avec plusieurs personnes
Le même formulaire peut être utilisé par plusieurs personnes :
- Votre collègue graphiste
- Votre manager
- L'équipe créative
Toutes les réponses arrivent au même endroit !

---

## 🔧 Options Avancées (Optionnel)

### Personnaliser le message de confirmation

1. Dans Tally → **Settings** → **After submit**
2. Choisissez **Show a message**
3. Personnalisez :
   ```
   ✅ Merci pour votre feedback !
   
   Votre commentaire a été envoyé à l'équipe Scarlet.
   Vous pouvez fermer cette fenêtre ou commenter un autre post.
   ```

### Limiter les réponses par personne

Si vous voulez qu'une personne ne puisse commenter qu'une fois par post :
1. **Settings** → **Access**
2. Activez **Limit responses**
3. Choisissez "One response per device"

### Ajouter une logique conditionnelle

Si le statut = "À revoir complètement" → demander plus de détails
1. Cliquez sur le champ "Commentaire"
2. **Logic** → **Show if...**
3. Condition : Status = "À revoir complètement"

---

## 🆘 Problèmes fréquents

### Le formulaire ne s'affiche pas
✓ Vérifiez que vous avez bien remplacé `VOTRE_FORM_ID`
✓ Vérifiez que le formulaire est **publié** dans Tally
✓ Videz le cache du navigateur (Ctrl+Shift+R)

### Les notifications n'arrivent pas
✓ Vérifiez votre email dans Settings → Notifications
✓ Regardez dans vos spams
✓ Testez avec un autre email

### Le numéro de post n'est pas capturé
✓ Vérifiez que le champ caché s'appelle bien `post`
✓ Vérifiez l'URL de l'iframe (doit contenir `&post=${postId}`)

---

## 📊 Tally.so Gratuit vs Pro

### Plan Gratuit (largement suffisant)
✅ **100 réponses / mois** (amplement suffisant)
✅ Formulaires illimités
✅ Notifications email
✅ Export Excel/CSV
✅ Thèmes personnalisés

### Plan Pro (12€/mois) - si besoin
- Réponses illimitées
- Logique conditionnelle avancée
- Intégrations (Slack, Notion, etc.)
- Branding personnalisé

➡️ **Le plan gratuit est parfait pour votre usage !**

---

## 🔗 Liens Utiles

- **Tally.so** : https://tally.so
- **Documentation** : https://tally.so/help
- **Support** : support@tally.so

---

## 📞 Besoin d'aide ?

Si vous rencontrez un problème :
1. Consultez ce guide
2. Vérifiez la section troubleshooting
3. Contactez le support Tally (très réactif !)

---

**Made with ❤️ for Scarlet Content Factory**

*Dernière mise à jour : Février 2026*
