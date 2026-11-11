# Tesoro del Sacré Coeur (AR.js + A-Frame)

Juego de búsqueda del tesoro con 3 marcadores AR de código de barras (matriz 3x3) pegados en puntos del edificio.

| # | Marcador | Dónde se pega | Pista que lleva a él | Función |
|---|----------|---------------|----------------------|---------|
| 1 | `barcode-1` | Cuadro de la Virgen | Al frente de la Capilla del Encuentro | Historia / desafío inicial |
| 2 | `barcode-2` | Carteles de reciclaje | Reciclaje de papel y cartón | Segunda pista |
| 3 | `barcode-3` | Máquina expendedora | Al frente de los baños del piso 1 | La llave; al completar, aparece el cofre |

## Estructura
- `index.html`: juego (A-Frame + AR.js, detección `mono_and_matrix` 3x3, pistas, progreso y temporizador).
- `marcadores.html`: hoja para imprimir los 3 marcadores (uno por hoja A4).
- `markers/barcode-{1,2,3}.png`: marcadores oficiales de ARToolKit (Matrix code 3x3).

## Imprimir
Abrir `https://<usuario>.github.io/<repo>/marcadores.html` e imprimir. Cada marcador de ~10-15 cm con borde blanco alrededor, en papel mate.

## Probar en casa
No hace falta estar en el edificio: abrir `marcadores.html` en la compu (o imprimirlos) y apuntar con el celular abierto en el juego, en orden 1 → 2 → 3.

## Publicar en GitHub Pages
1. Settings → Pages → Branch `main` / root.
2. La URL `https://<usuario>.github.io/<repo>/` es el entregable (HTTPS necesario para la cámara).
3. Cada push a `main` se publica solo en 1-3 minutos.
