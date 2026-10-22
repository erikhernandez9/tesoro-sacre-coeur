# Tesoro del Sacré Coeur (AR.js + A-Frame)

Juego de búsqueda del tesoro con 3 marcadores:

| # | Marcador | Función |
|---|----------|---------|
| 1 | HIRO | Historia / desafío inicial |
| 2 | KANJI | Segunda pista |
| 3 | Barcode 5 (matriz 3x3) | La llave; al completar, aparece el cofre |

Imágenes para imprimir (repo AR.js):
- Hiro: https://raw.githubusercontent.com/AR-js-org/AR.js/master/data/images/HIRO.jpg
- Kanji: https://raw.githubusercontent.com/AR-js-org/AR.js/master/data/images/kanji.png (o el patrón en `aframe/examples/image-tracking`/`data/data`)
- Barcode 5: https://github.com/AR-js-org/AR.js/tree/master/data/images (carpeta de barcodes) o generador en https://au.gmented.com/app/marker/marker.php (Matrix 3x3, valor 5)

Imprimir y colocar en distintos lugares del edificio.

## Publicar en GitHub Pages
1. Subir `index.html` a un repo nuevo.
2. Settings → Pages → Branch `main` / root.
3. La URL `https://<usuario>.github.io/<repo>/` es el entregable (HTTPS necesario para la cámara).
