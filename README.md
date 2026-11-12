# Tesoro del Sacré Coeur (AR.js + A-Frame)

**Historia: "Las 3 piezas del escudo".** El escudo original de la UCU se rompió en 3 piezas escondidas en el
Sacré Coeur. El jugador recolecta las 3 piezas (3 marcadores AR de código de barras 3x3) para reconstruirlo.

| # | Marcador | Dónde se pega | Pista que lleva a él | Pieza |
|---|----------|---------------|----------------------|-------|
| 1 | `barcode-1` | Cuadro de la Virgen | Pintura al frente de la Capilla del Encuentro | Pieza 1 (azul oscuro) |
| 2 | `barcode-2` | Carteles de reciclaje | Donde el papel y el cartón tienen segunda vida | Pieza 2 (dorada) |
| 3 | `barcode-3` | Máquina expendedora | Máquina hambrienta frente a los baños del piso 1 | Pieza 3 (azul claro) |

Al juntar las 3, aparece el escudo completo girando y la pantalla final con el tiempo.

## Estructura
- `index.html`: juego (A-Frame + AR.js, detección `mono_and_matrix` 3x3, historia, inventario de piezas, pistas y temporizador).
- `game.css`: estilos del juego (tema Hum: papel crema con grano, controles de cartulina, fuente Chillax). Los colores de las piezas 3D salen de sus tokens `--color-piece-*` vía `data-color`.
- `tokens.css` / `base.css`: tokens de diseño (colores OKLCH, espaciado, tipografía) y reglas base, generados con Hallmark. `.hallmark/` guarda el registro del rediseño.
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
