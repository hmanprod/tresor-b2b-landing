# Plan complet d’amélioration — Landing Page B2B

## 1. Objet du document

Ce document définit la feuille de route de refonte de la landing page B2B Trésor d’Épices afin d’augmenter les demandes qualifiées de Kits Découverte Pro, tout en renforçant la cohérence avec le site public [tresordepices.fr](https://www.tresordepices.fr/).

Le plan s’appuie sur :

- l’audit de la structure actuelle dans `landing-page-b2b.html` ;
- les captures d’écran de la landing page et du site public ;
- le positionnement et le funnel définis dans `PLAN.md` ;
- une lecture conversion, identité de marque, accessibilité et responsive.

Les captures fournies sont considérées comme des références visuelles à analyser, et non comme des instructions techniques à exécuter.

## 2. Décision stratégique

La landing page doit conserver son objectif unique : transformer un trafic froid issu du cold email et d’Instagram en demandes de Kits Découverte Pro.

La direction recommandée est une combinaison de deux univers :

1. **Conversion B2B** : message explicite, SIRET, sélection par métier, formulaire qualifiant et délais de traitement.
2. **Signature Trésor d’Épices** : brun chocolat, vert producteur, photographie sensorielle, origine Madagascar, ton premium et éditorial.

La page ne doit plus ressembler à une landing page SaaS générique. Elle doit donner l’impression d’un parcours professionnel proposé par une maison d’épices premium.

## 3. Objectifs

### Objectif principal

Obtenir davantage de demandes qualifiées de Kits Découverte Pro auprès d’établissements immatriculés.

### Objectifs secondaires

- Faire comprendre l’offre en moins de cinq secondes.
- Établir la légitimité de Trésor d’Épices avant de demander des informations.
- Réduire la friction du formulaire initial.
- Qualifier les prospects sans donner l’impression d’un formulaire administratif lourd.
- Présenter clairement la différence entre les quatre kits.
- Préparer une intégration CRM, Brevo et WhatsApp.
- Garantir une expérience cohérente sur desktop et mobile.

## 4. Diagnostic visuel actuel

### Forces à conserver

- Le hero est immédiatement compréhensible.
- Le vert du CTA est très visible.
- Les bénéfices « Direct Sambava », « SIRET requis » et « traitement sous 24 h » sont bien exposés.
- La barre de réassurance facilite la lecture rapide.
- La sélection par secteurs est pertinente pour un prospect B2B.
- Le formulaire est organisé en sections et possède une hiérarchie claire.
- Le CTA final sombre fonctionne bien et rappelle l’univers du site public.

### Écarts avec le site public

Le site public possède une identité plus éditoriale :

- hero brun chocolat ;
- grands titres avec contraste vert/blanc ;
- photographie immersive de la plantation ;
- mise en page plus luxueuse et moins encadrée ;
- boutons plus sobres et moins arrondis ;
- narration autour de l’origine, de l’expertise et du produit.

La landing page actuelle utilise davantage :

- des cartes blanches avec ombres ;
- des badges flottants ;
- des boutons en forme de pilule ;
- des icônes Font Awesome très présentes ;
- des blocs de réassurance fonctionnels.

Le résultat est professionnel, mais trop proche d’un modèle de landing page B2B standard.

### Problèmes de conversion

- Le formulaire demande trop d’informations au premier contact.
- Le mot « gratuit » est fort, mais les conditions d’éligibilité et d’expédition doivent être explicitées plus tôt.
- Le CTA « Tarifs Professionnels PDF » crée un second parcours concurrent.
- La page manque d’une section claire « Comment ça marche ? ».
- Les preuves sont déclaratives mais peu documentées.
- Les mêmes visuels sont réutilisés pour les différents métiers.
- Le parcours de confirmation est simulé côté front-end et n’est pas encore relié à un CRM.

### Problèmes de cohérence visuelle

- Le header de la landing page ne reprend pas suffisamment la signature du header public.
- Les boutons pilules sont trop éloignés du langage graphique du site principal.
- Le produit est présenté de façon très propre, mais peu sensorielle.
- Le brun chocolat, très identitaire sur le site public, est presque absent du hero B2B.
- Les nombreuses bordures, cartes et ombres rendent la page plus « outil » que « maison gastronomique ».

## 5. Nouvelle direction artistique

### Palette recommandée

Conserver le vert actuel comme couleur d’action, mais réintroduire le brun de marque comme couleur structurante.

```css
--brand-green: #4aa84f;
--brand-green-dark: #32843a;
--brand-brown: #2b1d1d;
--brand-brown-dark: #17100f;
--brand-cream: #f7f6f1;
--brand-white: #ffffff;
--brand-gold: #b8872d;
--brand-text: #211d1d;
--brand-muted: #7b817d;
```

### Règles de style

- Utiliser le brun chocolat pour le hero, la section origine ou le CTA final.
- Utiliser le vert principalement pour les actions, validations et éléments actifs.
- Réserver l’or/ambre aux labels premium et aux détails de réassurance.
- Réduire les ombres et éviter l’accumulation de cartes flottantes.
- Remplacer les rayons de 50 px des boutons par des rayons de 4 à 10 px.
- Garder de grands espaces, mais réduire les zones vides inutiles.
- Limiter les icônes aux éléments qui nécessitent une lecture rapide.

### Typographie

Conserver les familles déjà prévues, Outfit et Montserrat, afin de limiter les dépendances supplémentaires.

- H1 : Outfit 700/800, très grand, maximum deux ou trois lignes.
- H2 : Outfit 700, plus court et orienté bénéfice.
- Corps : Montserrat 400/500, largeur de ligne limitée à 620–680 px.
- Labels : Montserrat 600/700, capitales uniquement pour les petits labels.
- Éviter les longs textes en capitales dans les champs et titres de formulaire.

## 6. Architecture cible de la page

### Section 1 — Header B2B

Contenu :

- logo Trésor d’Épices suffisamment grand pour être identifiable ;
- badge discret « Professionnels » ou « Pro & Chefs » ;
- ancres : Kits par métier, Engagements, Comment ça marche, FAQ ;
- CTA : « Demander mon kit ».

Décisions :

- conserver un header sticky ;
- réduire le nombre de liens ;
- masquer les liens secondaires sur mobile ;
- afficher un bouton CTA compact mais toujours accessible.

### Section 2 — Hero de conversion

Structure recommandée :

- colonne gauche : promesse et bénéfices ;
- colonne droite : photographie réelle du kit ou composition de produits ;
- fond brun chocolat ou fond crème avec un bandeau brun partiel ;
- CTA principal : « Recevoir mon Kit Découverte Pro » ;
- CTA secondaire : « Voir ce que contient le kit ».

Proposition de copy :

> Testez la vanille et les épices de Madagascar dans votre établissement.

Sous-titre :

> Recevez un Kit Découverte Pro adapté à votre métier, réservé aux établissements immatriculés.

Réassurance immédiate :

- SIRET requis ;
- validation sous 24 h ;
- échantillons et tarifs professionnels ;
- expédition selon conditions annoncées.

À éviter :

- une promesse « gratuit » sans préciser l’éligibilité ;
- des badges qui recouvrent le produit ;
- des déclarations comme « taux de vanilline certifié » sans preuve accessible.

### Section 3 — Preuves de confiance

Remplacer la simple ligne d’icônes par quatre preuves plus concrètes :

1. **Origine** — production familiale à Madagascar / Sambava.
2. **Traçabilité** — suivi de la plantation au produit fini.
3. **Qualité professionnelle** — formats, conservation et fiches techniques.
4. **Accompagnement** — interlocuteur commercial et délai de réponse.

Chaque preuve doit être accompagnée d’un détail vérifiable ou d’un lien vers une explication.

### Section 4 — Comment ça marche ?

Créer la section manquante prévue dans `PLAN.md`.

```text
1. Choisissez votre secteur
2. Renseignez votre établissement et votre SIRET
3. Recevez la validation et votre Kit Découverte Pro
```

Cette section doit apparaître avant le formulaire pour réduire l’incertitude.

### Section 5 — Choix du kit par métier

Conserver les quatre segments :

- Restaurateurs & Chefs ;
- Artisans Glaciers & Pâtissiers ;
- Épiceries Fines & Revendeurs ;
- Hôtellerie & Grands Comptes.

Améliorations :

- utiliser un visuel différent pour chaque secteur ;
- afficher trois bénéfices maximum par kit ;
- afficher le contenu principal sans obliger l’utilisateur à lire un long paragraphe ;
- faire remonter le bouton vers le formulaire avec le kit déjà sélectionné ;
- conserver les onglets sur desktop, mais utiliser des cartes empilées ou un accordéon sur mobile.

### Section 6 — Preuve produit et origine

Ajouter une section inspirée du site public :

> De la plantation au produit fini.

Contenu recommandé :

- photo de la plantation ;
- photo du conditionnement ;
- court texte sur Madagascar et Sambava ;
- éléments de traçabilité ;
- lien vers la gamme complète uniquement si nécessaire.

Cette section donne une dimension émotionnelle à une page actuellement très administrative.

### Section 7 — Formulaire progressif

#### Étape 1 — Demande initiale

Champs recommandés :

- kit choisi ;
- nom de l’établissement ;
- SIRET ;
- email professionnel.

CTA :

> Vérifier mon établissement et demander le kit

#### Étape 2 — Qualification commerciale

À afficher après la première étape ou dans un second écran :

- nom et prénom ;
- fonction ;
- téléphone / WhatsApp ;
- volume estimé ;
- ville ;
- attentes particulières.

Cette séparation réduit la friction initiale tout en conservant les données nécessaires au lead scoring.

#### Règles UX du formulaire

- afficher une progression « Étape 1 sur 2 » ;
- préciser le temps estimé ;
- mettre le SIRET en évidence sans créer d’effet anxiogène ;
- ajouter une microcopie RGPD sous les champs ;
- utiliser `inputmode="numeric"` pour le SIRET ;
- contrôler le nombre de chiffres côté interface ;
- indiquer clairement si l’expédition est offerte ou non.

### Section 8 — FAQ

FAQ minimale recommandée :

1. Pourquoi le SIRET est-il requis ?
2. Que contient le kit ?
3. Quels sont les délais de validation ?
4. Les frais d’expédition sont-ils offerts ?
5. Puis-je demander un format ou un produit spécifique ?
6. Comment mes données sont-elles utilisées ?

La première question peut être ouverte par défaut. Les interactions doivent être accessibles au clavier.

### Section 9 — CTA final

Conserver le CTA sombre, qui est l’un des blocs les plus cohérents avec l’identité du site public.

Copy recommandée :

> Faites tester la qualité Trésor d’Épices dans votre établissement.

Sous-texte :

> Demandez votre kit professionnel en moins d’une minute. Nous vérifions votre établissement sous 24 h.

CTA :

> Demander mon Kit Découverte Pro

### Section 10 — Footer

Ajouter :

- mentions légales ;
- politique de confidentialité ;
- conditions du Kit Découverte Pro ;
- contact commercial ;
- WhatsApp professionnel si disponible ;
- lien B2C placé en dernier et visuellement secondaire.

## 7. Recommandations spécifiques à partir des captures

### Landing page

- Le hero est lisible, mais le titre occupe beaucoup d’espace vertical : vérifier sa hauteur sur laptop.
- La composition produit est trop blanche et manque de contraste avec le fond clair.
- Le premier CTA est pertinent, mais son libellé peut être plus direct.
- Le CTA PDF attire beaucoup l’attention et détourne du parcours principal.
- La barre de preuves est propre, mais les preuves sont trop similaires visuellement.
- La section métiers est claire, mais très espacée.
- Le formulaire est visuellement sérieux, mais semble long avant même sa lecture complète.
- Le CTA final est cohérent, mais arrive tard après un parcours déjà très long.

### Site public

Le site public fournit plusieurs éléments à reprendre :

- hero brun chocolat ;
- grands titres à contraste vert/blanc ;
- mise en avant de la plantation ;
- sections éditoriales avec beaucoup d’espace ;
- CTA verts plus sobres ;
- narration « origine → produit → expertise → contact ».

À ne pas reproduire :

- les images manquantes visibles dans certaines zones de la capture ;
- les cartes produits sans visuel chargé ;
- les textes alternatifs affichés à la place des images ;
- les sections trop longues sans CTA intermédiaire.

## 8. Accessibilité et responsive

### Desktop

- tester à 1280 px, 1440 px et 1920 px ;
- empêcher les badges flottants de sortir de l’écran ;
- vérifier que le header ne masque pas les ancres ;
- limiter les lignes de texte à une largeur confortable ;
- contrôler la hauteur totale du formulaire.

### Mobile

- header avec logo compact et CTA court ;
- hero en une colonne ;
- image produit sous le CTA ;
- boutons pleine largeur ;
- preuves en grille de deux colonnes puis une colonne ;
- onglets remplacés par accordéon ou cartes ;
- formulaire en une seule colonne ;
- CTA sticky bas d’écran uniquement si non intrusif.

### Accessibilité technique

- remplacer les `div` cliquables par des boutons ;
- ajouter `aria-expanded`, `aria-controls` et `aria-selected` ;
- gérer le focus visible ;
- associer chaque `label` à son champ ;
- ajouter une fermeture clavier aux modales ;
- fournir des textes alternatifs descriptifs ;
- vérifier les contrastes du vert, de l’or et du texte gris.

## 9. Fonctionnel et intégration

La version actuelle affiche une confirmation côté navigateur et écrit les données dans la console. Avant mise en ligne, il faut prévoir :

1. validation réelle du SIRET ;
2. envoi vers Brevo ou CRM ;
3. capture des paramètres UTM ;
4. email de confirmation ;
5. notification interne à l’équipe commerciale ;
6. lien WhatsApp ou prise de rendez-vous sur la page de remerciement ;
7. gestion des erreurs et des doublons ;
8. consentement RGPD enregistré avec la demande.

Les données sensibles ne doivent pas être exposées dans la console du navigateur en production.

## 10. Plan d’exécution par phases

### Phase 1 — Fondations de marque

- valider palette, rayons, ombres et typographie ;
- intégrer le brun chocolat du site public ;
- redéfinir les styles de boutons ;
- revoir le header et le footer ;
- choisir les visuels définitifs.

### Phase 2 — Refonte du contenu et de la structure

- réécrire le hero ;
- ajouter « Comment ça marche ? » ;
- ajouter origine et traçabilité ;
- réduire les textes des kits ;
- clarifier les conditions du kit gratuit ;
- revoir la FAQ.

### Phase 3 — Réduction de la friction

- transformer le formulaire en deux étapes ;
- simplifier le CTA PDF ;
- ajouter la progression ;
- ajouter les microcopies de confiance ;
- mettre en place la page de remerciement.

### Phase 4 — Qualité technique

- corriger les interactions accessibles ;
- tester les breakpoints ;
- optimiser les images ;
- vérifier les liens et les ancres ;
- connecter le formulaire au CRM ;
- tester les erreurs de validation.

### Phase 5 — Mesure et optimisation

- installer les événements analytics ;
- mesurer les clics CTA ;
- mesurer le début et la complétion du formulaire ;
- mesurer les abandons par champ ;
- tester deux versions du hero ;
- tester formulaire court contre formulaire long.

## 11. Événements de mesure recommandés

```text
landing_view
hero_cta_click
catalogue_cta_click
sector_selected
form_started
form_step_1_completed
form_step_2_started
form_submitted
form_error
faq_opened
whatsapp_click
```

Paramètres à conserver :

- `utm_source` ;
- `utm_medium` ;
- `utm_campaign` ;
- métier sélectionné ;
- statut du formulaire ;
- type de kit ;
- device et breakpoint.

## 12. Critères d’acceptation

La refonte pourra être considérée comme prête lorsque :

- la promesse est comprise sans scroller ;
- le hero est cohérent avec le site public ;
- le CTA principal est clairement dominant ;
- le formulaire initial contient au maximum quatre champs obligatoires ;
- le parcours complet est utilisable au clavier ;
- la page est lisible sur mobile, tablette et desktop ;
- chaque secteur possède un visuel pertinent ;
- les conditions du kit sont explicites ;
- les mentions RGPD sont présentes ;
- aucune image ne se retrouve cassée ;
- aucune donnée prospect ne reste dans la console ;
- les événements analytics sont vérifiables ;
- une confirmation réelle est envoyée après soumission.

## 13. Priorité finale

### Priorité immédiate

1. Refaire le hero dans l’univers brun/vert du site public.
2. Réduire le formulaire initial.
3. Ajouter le processus en trois étapes.
4. Remplacer les visuels répétés.
5. Clarifier les conditions du « gratuit ».

### Priorité haute

6. Connecter le formulaire au CRM.
7. Ajouter preuves, traçabilité et origine.
8. Corriger le responsive mobile.
9. Corriger l’accessibilité des onglets, FAQ et modales.

### Priorité secondaire

10. Mettre en place les tests A/B.
11. Ajouter WhatsApp et prise de rendez-vous.
12. Affiner les animations et micro-interactions.

## Conclusion

La landing page dispose déjà d’une base solide : le positionnement est clair, la structure est lisible et la proposition B2B est bien identifiée.

La prochaine étape n’est pas d’ajouter davantage de blocs, mais de renforcer trois éléments :

1. **la signature visuelle Trésor d’Épices** ;
2. **la confiance avant la collecte de données** ;
3. **la simplicité du premier contact**.

La version cible doit être plus sensorielle que la maquette actuelle, plus courte dans son parcours et plus concrète dans ses preuves.
