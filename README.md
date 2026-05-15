# LuxeFinish

Site web statique pret pour GitHub et Vercel.

## Publier

1. Creer un depot GitHub.
2. Ajouter ces fichiers dans le depot.
3. Dans Vercel, choisir **Add New Project** puis importer le depot GitHub.
4. Garder les reglages par defaut: Vercel detectera automatiquement le site statique.

## Connexions deja faites

- Navigation interne vers les sections du site.
- Boutons de soumission connectes au formulaire.
- Upload photo pour une estimation IA de demonstration.
- Formulaire de contact qui ouvre un courriel vers `contact@luxefinish.ca`.

Pour recevoir les demandes sans ouvrir l'application courriel du visiteur, il faudra ensuite connecter un vrai service de formulaire comme Vercel Forms, Formspree, Resend ou une fonction serverless.

## Tester localement

Avec Node.js:

```bash
node server.mjs
```

Puis ouvrir `http://127.0.0.1:4173`.
