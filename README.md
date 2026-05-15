# Eco Pure – Site Web Entretien Ménager Longueuil

Site web responsive (mobile + desktop) pour Eco Pure, service d'entretien ménager écologique à Longueuil.

## Structure des fichiers

```
ecopure/
├── index.html        ← Page principale (accueil)
├── services.html     ← Page services (avec ancres)
├── vercel.json       ← Config Vercel
└── README.md
```

## Pages & fonctionnalités

### index.html (page principale)
- ✅ Navigation responsive (burger menu mobile)
- ✅ Hero section avec image de fond
- ✅ Formulaire d'estimation en 3 étapes
- ✅ Calculateur de prix instantané (desktop)
- ✅ Section services (liens vers services.html)
- ✅ Section avant/après
- ✅ Témoignages
- ✅ FAQ avec accordéon
- ✅ Footer complet avec liens
- ✅ FAB téléphone (mobile)
- ✅ Animations scroll fade-in
- ✅ Toast notifications

### services.html
- ✅ Navigation identique
- ✅ Quick-nav avec ancres (#residentiel, #commercial, etc.)
- ✅ 5 services complets avec prix
- ✅ Images pour chaque service
- ✅ CTA vers formulaire

## Déploiement GitHub + Vercel

### 1. Pousser sur GitHub
```bash
git init
git add .
git commit -m "feat: site Eco Pure complet"
git remote add origin https://github.com/TON-USERNAME/ecopure.git
git push -u origin main
```

### 2. Déployer sur Vercel
1. Aller sur vercel.com → "New Project"
2. Importer ton repo GitHub `ecopure`
3. Framework Preset: **Other** (pas de build needed)
4. Root Directory: `.` (racine)
5. Cliquer "Deploy"

### 3. Variables à personnaliser
- Numéro de téléphone: `(450) 555-0123` → ton vrai numéro
- Email: `bonjour@ecopure.ca` → ton vrai email
- Pour le formulaire en production: connecter à un service comme Formspree ou EmailJS

## Formulaire en production (optionnel)

Pour recevoir les soumissions par email, remplacer la fonction `submitForm()` dans index.html:

```javascript
// Avec Formspree (gratuit jusqu'à 50 soumissions/mois)
// 1. Créer compte sur formspree.io
// 2. Créer un form, obtenir l'ID
// 3. Dans submitForm(), envoyer les données:

const response = await fetch('https://formspree.io/f/TON_FORM_ID', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    type: document.getElementById('form-type').value,
    rooms: selectedRooms,
    // ... autres champs
  })
});
```
