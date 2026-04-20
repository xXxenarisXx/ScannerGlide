# Glide-QR-Scanner

Application web minimale qui scanne des QR codes et ouvre l'URL scannée dans le navigateur.

Elle utilise la bibliothèque [`html5-qrcode`](https://github.com/mebjas/html5-qrcode) via CDN.

## URL de l'application

https://loqode.github.io/Glide-QR-Scanner/

## Fonctionnalités

- Utilise la caméra de l'appareil (caméra arrière par défaut) pour scanner les QR codes
- Affiche une superposition plein écran avec les données scannées
- Bouton **Open** pour naviguer vers l'URL scannée
- Bouton **Cancel** pour fermer la superposition et reprendre le scan
- Met le scan en pause pendant que la superposition est affichée (la caméra reste active)

## Utilisation

1. Ouvrir l'URL de l'application.
2. Autoriser l'accès à la caméra.
3. Pointer la caméra arrière vers un QR code contenant une URL.
4. L'URL décodée apparaît dans une superposition.
5. Appuyer sur **Open** pour naviguer vers l'URL, ou **Cancel** pour scanner à nouveau.

Pour ignorer la superposition de confirmation et ouvrir l'URL immédiatement lors du scan, ajouter `?confirm=0` :

https://loqode.github.io/Glide-QR-Scanner/?confirm=0

## Utilisation dans Glide

1. Dans l'éditeur de mise en page Glide, ajouter un composant **Web Embed**.
2. Coller l'URL de l'application comme source.
3. (Optionnel) Ajouter `?confirm=0` à l'URL pour ouvrir les liens scannés sans confirmation.
4. Ouvrir l'application Glide sur le téléphone, autoriser l'accès à la caméra et scanner un QR code contenant une URL.

## Notes

- Le contenu du QR code **doit être une URL valide** (ex. `https://example.com`). Du texte brut affichera une erreur de validation.
- L'accès à la caméra nécessite HTTPS — GitHub Pages sert l'application en HTTPS par défaut.
