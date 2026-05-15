# Vendly Landing — Déploiement

Landing page pour vendlypay.com — prête à déployer sur Vercel.

## 🚀 Déploiement en 5 minutes

### Option 1 — Via Vercel CLI (recommandé)

```bash
cd C:\Users\igork\vendly-site
npx vercel
```

Suis les questions :
- Set up and deploy? **Y**
- Which scope? (ton compte)
- Link to existing? **N**
- Project name? **vendly**
- Directory? **./**
- Override settings? **N**

➜ Ton site est en ligne en 30 secondes ! Tu reçois une URL `vendly-xxx.vercel.app`

### Option 2 — Via interface Vercel (drag & drop)

1. Va sur [vercel.com/new](https://vercel.com/new)
2. Choisis "Browse all templates" → "Other"
3. **Drag & drop ce dossier complet** `vendly-site/`
4. Clique "Deploy"
5. ✅ En ligne en 30 secondes

### Option 3 — Via GitHub

```bash
cd C:\Users\igork\vendly-site
git init
git add .
git commit -m "Initial landing"
git remote add origin https://github.com/[username]/vendly-landing.git
git push -u origin main
```

Puis sur Vercel : "Import Git Repository" → Sélectionne vendly-landing → Deploy

## 🌐 Connecter ton domaine vendlypay.com

Une fois déployé sur Vercel :

1. Dashboard Vercel → ton projet → **Settings → Domains**
2. Tape `vendlypay.com` → **Add**
3. Vercel te donne 2 enregistrements DNS à configurer

Sur ton registrar Camnic.cm :
- Type **A** → Name `@` → Value `76.76.21.21`
- Type **CNAME** → Name `www` → Value `cname.vercel-dns.com`

⏱️ Propagation DNS : 1-24h

## ✉️ Connecter le formulaire (Formspree gratuit)

1. Va sur [formspree.io](https://formspree.io) → crée un compte gratuit
2. New form → "Vendly Waitlist"
3. Copie l'endpoint (ex: `https://formspree.io/f/abc123`)
4. Dans `index.html`, cherche `action=` du formulaire
5. Remplace par `action="https://formspree.io/f/abc123"`
6. Redéploie

**Gratuit jusqu'à 50 submissions/mois** — largement suffisant pour démarrer.

## 📊 Analytics (Vercel Analytics gratuit)

1. Dashboard Vercel → Analytics → **Enable**
2. C'est tout — gratuit jusqu'à 2 500 events/mois

## 🎯 Mesures à suivre

- Visiteurs uniques / jour
- Taux de conversion (waitlist signups / visiteurs)
- Source du trafic (WhatsApp, Instagram, etc.)
- Pages les plus vues
- Temps moyen sur la page
