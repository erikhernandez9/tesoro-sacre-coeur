# Tesoro del Sacré Coeur (AR.js + A-Frame)

Juego de búsqueda del tesoro con 3 puntos reales del edificio. Usa **image tracking (NFT)** de AR.js:
no hay que imprimir marcadores, la cámara reconoce directamente el objeto.

| # | Punto | Pista que lleva a él | Función |
|---|-------|----------------------|---------|
| 1 | Cuadro de la Virgen | Al frente de la Capilla del Encuentro | Historia / desafío inicial |
| 2 | Carteles de reciclaje (papel y cartón) | Reciclaje de papel y cartón | Segunda pista |
| 3 | Máquina expendedora | Al frente de los baños del piso 1 | La llave; al completar, aparece el cofre |

## Estructura
- `index.html`: juego (A-Frame + AR.js NFT, lógica de progreso, pistas y temporizador).
- `markers/src/*.png`: fotos fuente de cada punto (ya rotadas, 750x1000).
- `markers/<nombre>.{iset,fset,fset3}`: descriptores NFT generados desde las fotos. **Requeridos para que funcione.**

## Generar los descriptores NFT
Con [NFT-Marker-Creator](https://github.com/webarkit/Nft-Marker-Creator-App) (Node >= 20.17):

```bash
git clone https://github.com/webarkit/Nft-Marker-Creator-App.git && cd Nft-Marker-Creator-App && npm install
cd src
node NFTMarkerCreator.js -i /ruta/al/repo/markers/src/cuadro.png
node NFTMarkerCreator.js -i /ruta/al/repo/markers/src/reciclaje.png
node NFTMarkerCreator.js -i /ruta/al/repo/markers/src/expendedora.png
```

Copiar los `.iset/.fset/.fset3` resultantes (`output/`) a `markers/` con los nombres `cuadro`, `reciclaje`, `expendedora`.
Alternativa sin Node: https://carnaux.github.io/NFT-Marker-Creator/

## Ajustar contenido 3D
Las unidades del contenido dentro de `<a-nft>` dependen del tamaño/DPI de la imagen. Si los objetos salen muy
grandes/chicos o fuera de lugar, ajustar `scale` y `position` en `index.html`.

## Publicar en GitHub Pages
1. Subir el repo a GitHub (incluida la carpeta `markers/`).
2. Settings → Pages → Branch `main` / root.
3. La URL `https://<usuario>.github.io/<repo>/` es el entregable (HTTPS necesario para la cámara).

## Consejos de uso
- Buena luz, apuntar de frente al objeto y a ~1-2 m.
- La expendedora y el cuadro deben reconocerse sin reflejos fuertes encima.
