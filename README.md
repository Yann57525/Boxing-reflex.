# Boxing Reflex V1 — PWA personnelle

Application gratuite de boxe anglaise en français : chronomètre, coach vocal aléatoire, défenses, jeu de jambes, réflexes visuels et statistiques stockées localement.

## Publier gratuitement en HTTPS avec GitHub Pages

1. Créer un compte gratuit sur https://github.com (si nécessaire).
2. Créer un dépôt **public** intitulé `boxing-reflex`.
3. Décompresser l'archive, puis ajouter **tous les fichiers du dossier `boxing-reflex`** à la racine du dépôt (index.html, app.js, style.css, sw.js, manifest.webmanifest, les icônes).
4. Ouvrir **Settings → Pages → Build and deployment → Deploy from a branch**. Choisir `main` et `/ (root)`, puis **Save**.
5. Attendre la publication. L'adresse sera normalement `https://VOTRE_IDENTIFIANT.github.io/boxing-reflex/` (à adapter à votre identifiant et au nom réel du dépôt).
6. Sur iPhone : ouvrir cette adresse dans **Safari**, toucher **Partager → Sur l'écran d'accueil → Ajouter**. Lancer l'application depuis l'icône ajoutée.
7. Ouvrir l'application au moins une fois avec Internet pour charger et mettre en cache ses fichiers. Tester ensuite en mode avion.

GitHub Pages publie un dépôt public : le **code de l'application** est visible publiquement. Les statistiques ne sont **pas** publiées et restent stockées localement sur l'iPhone. Ne pas ajouter de données personnelles au dépôt.

## Fonctionnement et limites de la V1

- Chronomètre : rounds 10 s–30 min, repos 0–10 min, 1–20 rounds, départ 5 s, cloche début/fin, continu et sans chrono.
- Coach vocal : attaque, défense et jeu de jambes combinables, avec annonces complètes ou progressives et réglages indépendants. Voix française de synthèse iOS.
- Réflexes : réaction simple, identification de quatre coups, choix d'une défense ; séries par essais, durée ou libre ; statistiques en millisecondes. **L'animation du gant est schématique** et non une animation réaliste de technique de boxe.
- La reconnaissance et la défense sont des **tests de choix sur écran**, pas une détection des mouvements corporels par caméra.
- Les statistiques sont locales (localStorage). Pas d'export/import, conformément au cahier des charges. La suppression des données du site, de Safari ou de l'app peut les effacer.
- Les pauses suspendent l'ensemble des exercices. L'application se met en pause quand elle passe à l'arrière-plan, car iOS ne garantit ni le son ni les minuteries écran verrouillé.
- La voix française hors connexion dépend des voix présentes sur l'iPhone. Pour tester, utiliser Réglages → Tester la voix, puis activer le mode avion.
- Le verrouillage de l'écran est évité uniquement si l'API Wake Lock est disponible et autorisée. Sinon régler temporairement le verrouillage automatique d'iOS.
- Les exercices vocaux ne nécessitent pas de connexion après installation ; une voix iOS non disponible localement peut toutefois ne pas fonctionner hors ligne.
- Les temps de réaction tactiles incluent la latence d'affichage et de saisie de l'iPhone : ce sont des indicateurs d'entraînement, pas des mesures scientifiques.
- Les combinaisons et déplacements « intelligents » sont fondés sur des règles simples, pas sur une évaluation biomécanique.

## Tester sur ordinateur (facultatif)

Depuis le dossier des fichiers : `python3 -m http.server 8000`, puis ouvrir `http://localhost:8000`.

## Confidentialité

Aucune bibliothèque externe, aucun suivi analytique, aucun compte. Les statistiques sont stockées dans le navigateur de l'appareil. Le code peut être hébergé sur GitHub Pages gratuitement.
