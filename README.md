# 📺 ¡Super Ángulos TV! 🎯 — Edición Smart TV LG (webOS)

Aplicación web interactiva contenida en **un único archivo HTML (`index.html`)**, lista para colgar en **GitHub Pages** y diseñada específicamente para el navegador web de **televisores Smart TV LG (webOS)**.

---

## ✨ ¿Qué puede hacer este programa y cómo está adaptado a TV LG?

### 1. Diseño Panorámico 16:9 para Televisores (1080p y 4K)
- **Sin barras de desplazamiento (`overflow: hidden`)**: Toda la interfaz ocupa exactamente `100vw x 100vh` usando unidades relativas (`vh` y `vw`), permitiendo leer textos, grados y dibujos perfectamente desde el sofá.
- **Optimizado para el mando LG Magic Remote y Cruceta**:
  - Botones gigantes con efectos luminosos al pasar el puntero (`:hover` y `:focus`).
  - **Sin campos de texto (`<input>`)**: Para evitar que se abra el molesto teclado virtual en pantalla del televisor LG, los jugadores se identifican como **Jugador 1** y **Jugador 2** y pueden cambiar su personaje animal (`🦊`, `🐼`, `🦁`, `🐸`, `🦄`, `🦖`...) con un solo clic del mando.
- **Compatibilidad total con motor Chromium de LG webOS**:
  - Evita funciones modernas no soportadas por versiones antiguas del navegador de LG (como `ctx.roundRect`), utilizando en su lugar la función propia `drawRoundedBox()` con curvas cuadráticas compatibles con cualquier Smart TV.

---

### 2. Los 6 tipos de ángulos en pizarra gigante
En la columna izquierda se muestra una pizarra de alto contraste (`760x420`) y en la columna derecha los 6 botones de respuesta:
1. **🐦 Ángulo Agudo (`< 90º`, ej. `40º`)**: Con arco azul y etiqueta grande de grados.
2. **📐 Ángulo Recto (`90º`)**: Con su esquina cuadrada verde clásica.
3. **🐘 Ángulo Obtuso (`> 90º`, ej. `120º`)**: Con arco naranja amplio.
4. **➖ Ángulo Llano (`180º`)**: Línea plana horizontal de media vuelta.
5. **👯 Ángulos Consecutivos**: Dos ángulos juntos que comparten vértice y el lado central (en color rojo).
6. **🌈 Ángulos Adyacentes**: Dos ángulos consecutivos cuyos lados exteriores forman una línea recta de `180º` (ej. `60º + 120º = 180º`).

---

### 3. Refuerzo Educativo con Sonidos (Web Audio API)
Cada vez que el niño hace clic con el mando en un botón, suena inmediatamente el sonido propio de ese ángulo en los altavoces del televisor:
- **Agudo** ➔ Sonido muy **agudo y cristalino** (flauta/pajarito).
- **Obtuso** ➔ Sonido muy **grave y profundo** (tuba/elefante).
- **Recto (`90º`)** ➔ Dos golpes firmes de onda cuadrada en esquina.
- **Llano (`180º`)** ➔ Nota larga, horizontal y plana.
- **Consecutivos** ➔ Dos notas vecinas seguidas (*Do → Mi*).
- **Adyacentes** ➔ Dos notas seguidas que se unen en un acorde plano de `180º`.

---

### 4. Modo 1 o 2 Jugadores con 12 Rondas por Jugador
- **Turnos alternos automáticos**:
  - *Ronda 1*: Jugador 1 ➔ Jugador 2.
  - *Ronda 2*: Jugador 1 ➔ Jugador 2... hasta completar las **12 rondas de cada jugador** (también permite elegir 6 o 10 rondas).
- **HUD inferior estilo concurso de TV**: Ilumina en dorado la tarjeta del jugador que tiene el turno activo en ese momento.
- **Laboratorio de Sonidos**: Permite practicar y escuchar todos los ángulos en la TV antes de empezar la partida.
