# 🚀 Grands explorateurs — le système solaire à toucher

Application de découverte du système solaire pour les tout-petits (dès 3 ans).
**Zéro texte à l'écran** : l'enfant explore en tapant sur les astres, tout passe
par l'image, le son et l'animation.

## Jouer

- **Écran de démarrage** : gros plan sur la Terre sous le titre, la fusée
  attend, un petit garçon et une petite fille montent à bord en sautillant,
  puis la caméra dézoome sur tout le système solaire.
- L'enfant **tape un astre** → la fusée décolle, voyage et **se met en
  orbite** autour de lui ; il tape un autre astre → elle s'y rend ; il tape
  la Terre → elle revient y **atterrir**.
- Chaque astre **parle** (voix enregistrées de la famille), avec musique
  d'ambiance en boucle et fondu enchaîné.
- Ambiance vivante : étoiles filantes, navette spatiale, satellite et ovni
  farceur qui fuit en zigzag s'il croise la fusée.
- **Espace parents** : cadenas en bas à droite (maintenir 3 s ou 3 petits
  taps) — son, musique, volume, plein écran.

## Sur iPad / iPhone

Ouvrir l'URL dans Safari, puis **Partager → « Sur l'écran d'accueil »** :
l'app s'installe avec son icône fusée et démarre plein écran, comme une
vraie application.

## Technique

Un seul fichier `index.html` autonome (aucune dépendance, aucun réseau) :
scène SVG animée, Web Audio pour les bruitages, moteur audio à deux niveaux
(enregistrements perso → sinon synthèse vocale). Fonctionne également en
local : `python3 -m http.server` puis ouvrir `http://localhost:8000`.
