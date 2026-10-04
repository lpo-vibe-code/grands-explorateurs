# 🚀 Le système solaire à toucher

Application de découverte du système solaire pour enfant dès 3 ans.
**Zéro texte à l'écran** : l'enfant explore en tapant sur les astres,
tout passe par l'image, le son et l'animation.

## Comment jouer

- **Écran de démarrage** : gros plan sur la Terre sous le titre
  **« Grands explorateurs »** (police Orbitron, ambiance espace — la Lune
  passe au-dessus du titre). La fusée attend, un petit garçon et une petite
  fille sautillent à côté. Au tap, ils montent à bord en petits bonds — et
  la caméra dézoome pour révéler tout le système solaire. C'est parti !
- L'enfant **tape n'importe quel astre** → la fusée décolle, traverse
  l'espace et **se met en orbite** autour de l'astre choisi.
- Au **premier décollage** uniquement : le nom de l'astre est prononcé,
  puis le compte à rebours (« 3… 2… 1… décollage ! ») pendant lequel la
  fusée tremble sur son pas de tir — puis envol.
- Il tape un **autre astre** → la fusée quitte son orbite et s'y rend.
- Il tape la **Terre** → la fusée revient et **atterrit en douceur**.
- Taper le même astre pendant l'orbite → pluie d'étincelles.
- Taper la Terre quand la fusée y est posée → petit saut de joie.
- Taper le vide → petites étincelles (jamais d'échec, jamais de punition).

Chaque tap prononce le nom de l'astre et une courte phrase de découverte.
Le message d'accueil (« Touche une planète pour jouer ! ») est joué à la
fin du dézoom de démarrage.

## Petites animations d'ambiance

Discret et espacé, pour émerveiller sans surstimuler :

- **Étoiles filantes** : une de temps en temps (toutes les 7 à 18 s),
  traînée lumineuse qui traverse une partie du ciel en diagonale.
- **La navette** : un petit vaisseau blanc traverse le système en slalom
  (première visite après ~20-45 s, puis toutes les 45 à 90 s). Elle passe
  **derrière** les planètes, comme si elle volait plus loin. Si elle croise
  la fusée de l'enfant : petit sursaut d'étincelles, et elle s'enfuit à
  toute vitesse hors du système solaire !
- **Le satellite** (rare) : un satellite à panneaux solaires traverse
  tout l'écran **très lentement**, feu rouge clignotant, sans interaction
  (toutes les 90 à 180 s). Un vrai moment de contemplation.
- **L'ovni** (très rare) : une soucoupe **vue de profil** — coque en
  lentille, dôme vert avec son petit extraterrestre, feux clignotants —
  au vol nerveux : zigzags, variations de vitesse, parfois presque l'arrêt,
  et elle se penche dans les virages (toutes les 2 à 4 min).
  S'il croise la fusée : surprise totale, "woop !" et fuite en zigzag
  serré avec traînée verte !

## Ouvrir l'application

Un seul fichier, rien à installer : ouvrez **index.html**
(double-clic → s'ouvre dans Safari/Chrome). Optimisé pour tablette,
fonctionne aussi à la souris sur ordinateur.

Pour l'installer sur iPad : copier le dossier dans Fichiers/iCloud,
ouvrir index.html dans Safari, puis Partager → "Sur l'écran d'accueil".

> Si un navigateur bloquait les sons depuis un fichier local, lancer
> un mini-serveur dans ce dossier : `python3 -m http.server`
> puis ouvrir `http://localhost:8000`.

## Son

- **Voix off** : vos enregistrements dans **audio/** (`mars.mp3`, `soleil.mp3`…)
  sont utilisés automatiquement ; à défaut, une voix de synthèse française.
- **Musique d'ambiance** : les morceaux du dossier **audio/** (`soundtrack.wav`,
  `space track.mp3`) jouent en boucle, enchaînés avec un fondu de 2 secondes.
  Volume et arrêt : **Espace parents** (bouton Musique + curseur de volume,
  réglage mémorisé).

## Espace parents

Le petit **cadenas** en bas à droite (il pulse doucement au démarrage).
Deux façons de l'ouvrir :

- **maintenir appuyé 3 secondes** (anneau de progression jaune), ou
- **3 petits taps rapides** (moins de 2 s entre chaque).

Le panneau contient :

- 🔊 couper / rétablir tout le son (voix + bruitages + musique)
- 🎵 couper / rétablir la musique d'ambiance
- 🎵 curseur de volume de la musique
- ⛶ plein écran

Les réglages sont mémorisés d'une session à l'autre.

## Technique

HTML/CSS/JS 100 % autonome, aucune dépendance, aucun réseau.
Scène SVG animée, bruitages générés par Web Audio, moteur audio à deux
niveaux (vos fichiers → sinon synthèse vocale).
