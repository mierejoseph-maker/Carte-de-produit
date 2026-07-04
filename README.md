# Carte-de-produit
Ce projet est une grille de cartes produits pour un marketplace fictif proposant des articles d'électronique, de vêtements, de livres et de nourriture congolaise.

L'objectif était de construire des cartes visuellement soignées, cohérentes dans leur espacement, et dotées d'interactions (survol, sélecteurs avancés) tout en gérant proprement la spécificité CSS.


📂 Structure du fichier

cartes-produits.html
└── <head>
    └── <style>          → Toutes les règles CSS (tokens, cartes, boutons, responsive)
└── <body>
    ├── .page-head        → Titre et intro de la page
    └── .grid             → Conteneur des cartes
        └── .card × 4     → Une carte par produit

Le fichier est autonome (un seul .html, CSS intégré) : il suffit de l'ouvrir dans un navigateur.


🧩 Composition d'une carte

Chaque carte (300 × 400px) contient :


Image du produit — zone .card__media (170px de hauteur)
Badge d'état — En stock, Promo -20%, Nouveau ou Rupture
Bouton favoris flottant (♡) positionné sur l'image
Catégorie du produit (étiquette discrète)
Nom du produit (police display)
Description courte, limitée à 2 lignes
Étoiles de notation avec nombre d'avis
Prix (avec prix barré en cas de promo)
Boutons d'action : Ajouter au panier (plein) + Favoris (contour rond)



✅ Critères techniques respectés


 Sélecteurs avancés : :hover (carte, boutons, favoris) et :nth-child(even) (décalage alterné des cartes dans la grille)
 Box model maîtrisé : padding, gap et margin cohérents dans .card__body, pas de chevauchement de marges
 Spécificité CSS gérée : une seule classe d'état (.is-disabled) pour la carte en rupture de stock, sans conflit entre sélecteurs de type et de classe
 Ombres et bordures : box-shadow au repos et au survol (--shadow-rest / --shadow-hover), border fine sur les cartes et les boutons secondaires
 4 cartes minimum avec variation : badges, prix, notes et états différents



✨ Effets d'interaction


Survol de carte : légère translation vers le haut + scale(1.03) + ombre plus profonde
Survol des boutons : changement de couleur, légère élévation
Survol du bouton favoris : agrandissement (scale)



🚀 Utilisation


Télécharger le fichier products.html
L'ouvrir dans un navigateur (Chrome, Firefox, Edge…)
Survoler les cartes et les boutons pour voir les interactions


Aucune installation, aucune dépendance à builder — tout fonctionne directement dans le navigateur.


🛠️ Technologies utilisées


HTML5 — structure sémantique (<article>, <section>)
CSS3 — variables (:root), Flexbox, box-shadow, transition, sélecteurs avancés
Google Fonts — Fraunces & Inter
Google - image de demonstration
