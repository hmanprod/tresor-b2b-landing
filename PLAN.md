# Plan Stratégique & Structure — Landing Page d'Acquisition B2B

## 1. Objectif & Positionnement
Transformer le trafic à froid (provenant du **Cold Email** et de la **Prospection Instagram**) en **demandes qualifiées de Kits Découverte Pro**.

- **Angle d'Acquisition** : *"Testez gratuitement la qualité de nos produits dans votre établissement."* (Approche d'invitation à tester / réduction maximale de la friction).
- **Cible B2B** : Établissements immatriculés (numéro SIRET/SIREN obligatoire pour valider la commande de kit).
- **Focus Funnel Unique** : 100% centré sur la commande du **Kit Découverte Pro**, sans liens de fuite vers la boutique B2C.

---

## 2. Architecture & Funnel de Conversion (10 Sections)

```
[Cold Email / Instagram DM]
         │ (Message Match : "Testez notre Vanille & Épices de Madagascar")
         ▼
 1. En-tête B2B Hermétique (Identité Trésor d'Épices + Menu ancres B2B + CTA direct)
 2. Hero Section (Message Match + Double CTA : Kit Découverte vs Tarifs PDF)
 3. Barre de Preuves & Réassurance Pro (Direct Sambava, Taux Vanilline, Sous-Vide, SIRET Requis)
 4. Offres & Kits Découverte par Secteur (Onglets interactifs + Synchro dynamique)
 5. Gammes de Produits Pros (Gousses Gourmet, Poivre Voatsiperifery, Épices d'exception)
 6. Processus en 3 Étapes (Formulaire SIRET -> Validation 24h -> Envoi Colissimo Pro 48h)
 7. Formulaire de Qualification B2B avec SIRET (Sélecteur visuel des 4 Kits par cartes)
 8. FAQ de Réassurance Acheteurs (Explication SIRET, délais, emballage sous-vite, traçabilité)
 9. CTA Final Dark & Rappel Engagement (Incitant au dépôt de dossier pro)
10. Footer Minimal B2B (Mentions RGPD & Vérification SIRET)
```

---

## 3. Détail des 4 Kits Découverte par Secteur

1. 🍽️ **Kit Restaurateurs & Chefs**
   - *Composition* : Gousses Vanille Bourbon Gourmet (14-16cm) + Poivre Voatsiperifery Sauvage + Grille tarifaire restauration HT.
2. 🍦 **Kit Artisans Glaciers & Pâtissiers**
   - *Composition* : Gousses d'extraction riches en vanilline + Échantillon Poudre / Extraits 100% naturels + Fiches techniques d'incorporation.
3. 🏬 **Kit Épiceries Fines & Revendeurs**
   - *Composition* : Tubes en verre de présentation sous étui cadeau + Baies roses & Épices + Grille de marge boutique & PLV.
4. 🏨 **Kit Hôtellerie & Grands Comptes**
   - *Composition* : Vanille Gourmet + Poivres rares VIP + Proposition de contrats d'approvisionnement et cadencement des stocks.

---

## 4. Indicateurs de Qualification B2B (Lead Scoring)

Le formulaire collecte les données essentielles pour prioriser les meilleurs comptes :
- **Identification Légale** : Nom d'établissement, Numéro SIRET / SIREN (14 chiffres).
- **Statut de l'Entreprise** : *En activité (besoin récurrent)*, *Ouverture prochaine (3 mois)*, *Recherche de nouveau fournisseur*.
- **Profil du Décisionnaire** : Nom, Prénom, Fonction (*Chef*, *Gérant*, *Directeur des Achats*, *Acheteur Épicerie*).
- **Coordonnées Directes** : Email Pro, Téléphone / WhatsApp direct, Canal de contact préféré (*WhatsApp*, *Téléphone*, *Email*).
- **Intention & Volume** : Kit Découverte sélectionné, Volume annuel estimé (*Test initial*, *<50 gousses/mois*, *50-200 gousses/mois*, *>200 gousses/mois*).

---

## 5. Intégration Technique & Automatisation (Prochaine Étape)

- **Connexion CRM / Brevo** :
  - Envoi automatique des données du formulaire vers une liste Brevo B2B (*Lead Scoring* basé sur le volume et le SIRET).
  - Déclenchement d'un email / message WhatsApp de confirmation automatique après validation du SIRET.
- **Tracking & UTM** :
  - Capture automatique des paramètres UTM dans les URLs (`utm_source=cold_email`, `utm_source=instagram_dm`, `utm_campaign=chefs_2026`).
- **Page de Remerciement (Thank You Page)** :
  - Redirection vers une page de confirmation avec bouton direct WhatsApp Pro et prise de rendez-vous téléphonique optionnelle.
