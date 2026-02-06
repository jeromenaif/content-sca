# ⚡ Quick Start - Tally.so pour Scarlet

## 🎯 Ce qui a changé

✅ **giscus (nécessite GitHub)** ❌  
✅ **Tally.so (aucun compte requis)** ✨

## 🚀 Configuration Express (10 minutes)

### 1. Créer le formulaire
👉 https://tally.so → Sign up → Create form

### 2. Ajouter 6 champs :
1. **Hidden field** : `post` (numéro auto)
2. **Short text** : Nom (optionnel)
3. **Multiple choice** : Statut (Validé / En attente / À revoir)
4. **Multiple choice** : Type de feedback
5. **Long text** : Commentaire
6. **Email** : Email (optionnel)

### 3. Personnaliser
- Theme : **Dark**
- Color : **#E61F13**
- Submit button : **Envoyer mon feedback**

### 4. Publier et copier le Form ID
Publish → Share → Embed → Copier le **Form ID** (ex: `wgbxQl`)

### 5. Mettre à jour le HTML
Ligne ~490 du fichier HTML :
```javascript
const tallyFormId = 'wgbxQl'; // Votre Form ID
```

## ✅ C'est tout !

Votre collègue pourra maintenant laisser des feedbacks **sans créer de compte**.

---

## 📧 Vous recevrez les notifications

Chaque nouveau feedback arrive par email avec :
- Numéro du post
- Statut (Validé/En attente/À revoir)
- Commentaire complet

Dashboard : https://tally.so → Responses

---

## 💡 Exemple de workflow

**Votre collègue** :
1. Ouvre le générateur
2. Clique sur "Post #3"
3. Scrolle vers le bas
4. Remplit : "Validé - Juste agrandir le titre"
5. Clique "Envoyer"

**Vous** :
1. Recevez l'email : "Nouveau feedback sur Publication #3"
2. Lisez : "Validé - Juste agrandir le titre"
3. Faites l'ajustement
4. ✅

---

Pour plus de détails → **TALLY_SETUP.md**
