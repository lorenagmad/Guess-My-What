# Guess My What?!

[English](README.md) · **Español**

Un juego de adivinar por equipos para el aula o para cualquier grupo. Un jugador se pone el móvil en la frente sin mirarlo y su equipo le explica la palabra que aparece en la pantalla sin decirla. Los sensores de movimiento del móvil detectan si ha acertado.

**Jugar:** https://lorenagmad.github.io/Guess-My-What/

Sirve para cualquier asignatura o tema, y también para actividades sociales: escribes tu propia lista de conceptos o la cargas desde una hoja de Google.

## Idiomas

El juego está en **español** y en **inglés**. El idioma se elige con los botones **Español / English** de la parte superior de la portada. La primera vez, el juego usa el idioma del dispositivo; después recuerda tu elección.

Al cambiar de idioma también se traducen los nombres de equipo por defecto, el nombre de partida por defecto y la lista de ejemplo. Los nombres y conceptos que hayas escrito tú se mantienen tal cual.

## Cómo se juega

1. **Prepara la partida.** Ponle nombre, escribe los conceptos y elige la modalidad y las opciones.
2. **Añade a los participantes** y pon a cada uno en un equipo. Cada equipo necesita al menos un participante.
3. **Lanza la moneda** para decidir qué equipo empieza.
4. **Jugad.** El jugador que indica la pantalla se pone el móvil en la frente, con la pantalla hacia su equipo y en horizontal. Un compañero toca la pantalla para empezar y el equipo le explica el concepto hasta que lo adivine o se acabe el tiempo.
5. **Mira el resultado.** La pantalla final muestra el ganador, la puntuación de cada equipo y todos los conceptos jugados, con quién los jugó y cuánto tardó.

La partida en curso se guarda en el dispositivo, así que puedes dejarla y continuarla después desde la portada.

## Modalidades

| Modalidad | Cómo funciona | Puntuación |
| --- | --- | --- |
| **Turnos** | Cada turno es un solo concepto con su propio tiempo (de 30 segundos a 2 minutos). | +1 por acierto y −1 por fallo. Eliges si el equipo que acierta sigue jugando o pasa el turno al otro; después de un fallo, siempre juega el otro equipo. |
| **Contrarreloj** | Cada equipo tiene una ronda con tiempo para adivinar todos los conceptos que pueda y luego juega el otro equipo. Eliges de 1 a 5 rondas por equipo. | +1 por cada acierto. Pasar un concepto puede no restar nada o restar 1 punto. |
| **Tres rondas** | Los mismos conceptos se juegan tres veces: **1.** se explican libremente, **2.** con una sola palabra, **3.** solo con mímica. Los equipos se turnan con tiempo; un concepto pasado vuelve al final del montón. Cuando se acaban los conceptos de una ronda, empieza la siguiente. | +1 por cada acierto. Pasar un concepto puede no restar nada o restar 1 punto. |

También puedes limitar cuántos conceptos se usan (5, 8, 10, 15, 20 por equipo, o todos).

## Conceptos

Escribe un concepto por línea. Cada línea puede llevar también **palabras prohibidas** y una **definición**, separadas por asteriscos:

```
Paraguas * lluvia, mojarse, abrir * Objeto que se abre para protegerse de la lluvia
```

- **Las palabras prohibidas** aparecen debajo del concepto durante el juego, para que el equipo sepa qué no decir. Si alguien dice una, el concepto cuenta como no acertado o se pasa. Puedes ocultarlas en la preparación. En **Tres rondas** solo se muestran en la primera ronda.
- **La definición** se guarda con cada concepto en el registro de actividad.
- Los repetidos se eliminan. El contador debajo de la lista indica cuántos conceptos tienen palabras prohibidas o definición.

Otras formas de llenar la lista:

- **Desde una hoja de Google:** comparte la hoja como «Cualquier persona con el enlace» y pega su dirección. La columna A es el concepto, la B las palabras prohibidas (separadas por comas) y la C la definición. Se salta una cabecera como «Conceptos».
- **Usar ejemplo:** 20 conceptos cotidianos, con palabras prohibidas y definiciones, en el idioma que hayas elegido.
- **Borrar la lista:** quita todos los conceptos. Tócalo dos veces para confirmar.

## Movimiento del móvil

| Modalidad | Acertado | No acertado o pasar |
| --- | --- | --- |
| Turnos | Pon el móvil boca abajo en la mesa | Pon el móvil boca arriba en la mesa |
| Contrarreloj y Tres rondas | Inclina el móvil hacia abajo | Inclina el móvil hacia arriba |

Usa **Probar el movimiento** en la pantalla de preparación antes de jugar. En iPhone, el navegador pide permiso para usar los sensores de movimiento al lanzar la moneda.

Si un móvil no tiene sensores de movimiento, o no responden, el juego muestra los botones **Acertado** y **No acertado** (o **Pasar**) durante cada turno. Puedes ocultarlos en la preparación.

Los sensores solo funcionan cuando el juego se abre desde su propia dirección con HTTPS, como el enlace de GitHub Pages de arriba. No funcionan dentro de vistas previas ni de páginas incrustadas.

## Registro de actividad (xAPI)

Para usarlo en clase, el juego puede guardar un registro de actividad en formato [xAPI](https://xapi.com/). Está desactivado por defecto.

- **Qué guarda:** el inicio de la partida (modalidad, equipos y sus participantes, número de conceptos, tiempo y si se muestran las palabras prohibidas), cada concepto jugado (quién, de qué equipo, si se acertó, cuánto tardó, cómo se marcó: sensor, botón o tiempo, la ronda, y sus palabras prohibidas y definición) y la puntuación final.
- **Identificación:** el nombre del participante siempre se pide. El correo y un DNI o documento pueden ser «No pedir», «Opcional» u «Obligatorio».
- **Consentimiento:** con el registro activado, el juego pide confirmar que los participantes saben que se guarda su actividad antes de poder empezar.
- **Descarga:** el registro se descarga como archivo `.json` desde la pantalla final, listo para importarlo en un Learning Record Store (LRS) o para analizarlo.
- **Formato:** los nombres de los campos y los valores de las respuestas son iguales en los dos idiomas, para poder analizar juntos registros de partidas en español y en inglés. Los nombres de los verbos y de las actividades se escriben en el idioma de la partida y se marcan con él (`es-ES` o `en-US`).

Para usar el juego fuera del aula, pide solo el nombre y deja el registro desactivado.

## Privacidad

Todo se queda en el dispositivo. La configuración, los participantes, la partida en curso y el registro de actividad se guardan en el navegador (`localStorage`) y nunca se envían a un servidor. El juego solo se conecta a internet para:

- cargar su tipografía (Nunito) desde Google Fonts,
- leer una hoja de Google, solo cuando la cargas.

## Diseño y accesibilidad

- Colores del logotipo de TELA UCA y una sola tipografía, Nunito, elegida para leerse a distancia.
- Los botones y los campos del formulario funcionan con el teclado y muestran el foco.
- Si el dispositivo tiene activado «reducir movimiento», se desactivan las animaciones y el confeti.
- Los modos claro y oscuro siguen la configuración del dispositivo.

## Publicarlo tú

Todo el juego es un único archivo, `index.html`, sin compilación ni dependencias que instalar.

- **En tu ordenador:** abre `index.html` en un navegador. Los sensores de movimiento necesitan HTTPS, así que para probarlo del todo en un móvil, publícalo primero.
- **En GitHub Pages:** en el repositorio, ve a **Settings → Pages**, elige **Deploy from a branch**, selecciona `main` y `/ (root)`, y guarda. El juego estará en `https://<usuario>.github.io/<repositorio>/`.

## Créditos

Creado por [TELA UCA](https://lorenagmad.github.io/tela_uca/) (Technology Enhanced Learning for All), Departamento de Ingeniería Informática, Campus de Jerez, Universidad de Cádiz.
