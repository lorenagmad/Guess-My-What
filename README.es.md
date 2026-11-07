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
- **Descarga:** el registro se descarga como archivo `.json` desde la pantalla final, listo para abrirlo en el [panel de análisis](#panel-de-análisis) o para importarlo en un Learning Record Store (LRS).
- **Formato:** los nombres de los campos y los valores de las respuestas son iguales en los dos idiomas, para poder analizar juntos registros de partidas en español y en inglés. Los nombres de los verbos y de las actividades se escriben en el idioma de la partida y se marcan con él (`es-ES` o `en-US`).

Para usar el juego fuera del aula, pide solo el nombre y deja el registro desactivado.

## Panel de análisis

El panel de análisis convierte los registros de actividad en un resumen de cómo ha jugado tu clase: qué conceptos han costado más, cómo ha ido cada partida y cómo le ha ido a cada participante. Es una página aparte que funciona entera en tu navegador: los archivos que cargas **no se suben a ningún sitio**.

**Abrirlo:** https://lorenagmad.github.io/Guess-My-What/panel.html

El panel está en **español** y en **inglés**, con los mismos botones **Español / English** que el juego, y se abre en el idioma que elegiste en el juego. Lee los registros de partidas jugadas en cualquiera de los dos idiomas.

### Paso a paso

1. **Antes de jugar, activa el registro.** En la pantalla de preparación, pon **Registro de actividad (xAPI)** en **Con registro**. Elige si se pide el correo y el DNI (con **No pedir** basta para el panel; el nombre o un apodo se pide siempre).
2. **Jugad la partida** como siempre.
3. **Descarga el registro** desde la pantalla final con **Descargar el registro (xAPI)**. Hazlo antes de empezar otra partida: el registro solo se guarda en el dispositivo hasta entonces. Obtendrás un archivo llamado `guess-my-what_….json`.
4. **Abre el panel** y arrastra los archivos al recuadro de líneas discontinuas, o pulsa **Elegir archivos**. Puedes cargar varios a la vez, de distintos grupos y días: se unen y se quitan los duplicados.
5. **Deja fuera a quien no deba contarse (opcional).** Abre **Excluir participantes** y escribe, uno por línea, el nombre o código con el que jugó cada uno (también vale su correo o su DNI). Consulta [Excluir participantes](#excluir-participantes).
6. **Consulta los resultados.** Con los filtros de arriba puedes ver una sola partida (o asignatura) o una sola modalidad.
7. **Exporta** lo que necesites en archivos CSV, que se abren con Excel o LibreOffice.

Para empezar de nuevo con otros archivos, pulsa **Vaciar**.

### Qué muestra

| Sección | Qué muestra |
| --- | --- |
| Resumen | Número de partidas, participantes y conceptos jugados, porcentaje de aciertos, tiempo mediano para acertar y cuántos conceptos se han fallado alguna vez. |
| **Repaso** | Los conceptos que más han costado, con su definición y sus palabras prohibidas, listos para comentarlos en clase. Se puede descargar en CSV o copiar. |
| **Tres rondas** | Solo en partidas de *Tres rondas*: cómo cambia el acierto al pasar de explicar libremente a una sola palabra y a la mímica. |
| **Conceptos** | Cada concepto: veces jugado, acertado, no acertado, pasado y tiempo mediano. Pulsa una columna para ordenar. |
| **Partidas** | Cada partida: fecha, nombre, modalidad, marcador final, conceptos jugados, acierto y duración. |
| **Jugadores** | Cada participante: equipo, conceptos que jugó con el móvil en la frente, acierto y tiempo mediano. |

### Ocultar los datos personales

La casilla **Ocultar datos identificativos** de la parte superior está **marcada por defecto**. Mientras lo esté, los nombres, correos y DNI se sustituyen por códigos (J-01, J-02…) en pantalla y en todas las exportaciones, y se ocultan los nombres de los archivos cargados. Desmárcala solo si necesitas saber quién es quién, por ejemplo para comentar sus resultados con un estudiante.

Ten en cuenta que:

- Los códigos se asignan cada vez que cargas archivos, por orden alfabético de los participantes. Si cargas otro conjunto de archivos, la misma persona puede recibir otro código.
- La ocultación solo afecta al panel. **Los archivos `.json` descargados siguen conteniendo lo que escribieron los participantes** (nombre o apodo y, si los pediste, correo y DNI). Guárdalos como cualquier otro dato de tus estudiantes, por ejemplo en el almacenamiento de tu institución, y bórralos cuando ya no los necesites.
- Para recoger los mínimos datos personales posibles, pide a los participantes que usen un apodo o un código en lugar de su nombre real, y deja el correo y el DNI en **No pedir**.
- Si vas a usar los datos para investigar, necesitas el consentimiento informado de los participantes y la aprobación que exija tu institución. Publica solo resultados agregados.

### Excluir participantes

Usa **Excluir participantes** cuando haya participantes que no deban contarse, por ejemplo estudiantes que no han dado su consentimiento para un estudio.

- Escribe un participante por línea: el nombre o código con el que jugó, o su correo o su DNI. Da igual usar mayúsculas o dejar espacios de más.
- Sus conceptos desaparecen del resumen, de todas las tablas y de todas las exportaciones. El panel indica cuántos participantes y conceptos se han dejado fuera, y avisa si alguna línea no coincide con nadie de los registros cargados.
- Puedes mantener marcada **Ocultar datos identificativos** todo el tiempo: el panel nunca muestra a quién corresponde cada línea.
- Los códigos (J-01, J-02…) se asignan solo a los participantes que quedan.
- La lista no se guarda. Si recargas la página, vuelve a escribirla.

## Privacidad

Todo se queda en el dispositivo. La configuración, los participantes, la partida en curso y el registro de actividad se guardan en el navegador (`localStorage`) y nunca se envían a un servidor. El panel de análisis lee en tu navegador los archivos que cargas y tampoco los envía a ningún sitio. El juego y el panel solo se conectan a internet para:

- cargar sus tipografías desde Google Fonts (no se envía ningún dato de las partidas),
- leer una hoja de Google, solo cuando la cargas.

## Diseño y accesibilidad

- Colores del logotipo de TELA UCA y una sola tipografía, Nunito, elegida para leerse a distancia.
- Los botones y los campos del formulario funcionan con el teclado y muestran el foco.
- Si el dispositivo tiene activado «reducir movimiento», se desactivan las animaciones y el confeti.
- Los modos claro y oscuro siguen la configuración del dispositivo.

## Publicarlo tú

Todo el juego es un único archivo, `index.html`, y el panel de análisis es otro, `panel.html`. No hay compilación ni dependencias que instalar.

- **En tu ordenador:** abre `index.html` en un navegador. Los sensores de movimiento necesitan HTTPS, así que para probarlo del todo en un móvil, publícalo primero.
- **En GitHub Pages:** en el repositorio, ve a **Settings → Pages**, elige **Deploy from a branch**, selecciona `main` y `/ (root)`, y guarda. El juego estará en `https://<usuario>.github.io/<repositorio>/` y el panel en `https://<usuario>.github.io/<repositorio>/panel.html`.

## Créditos

Creado por [TELA UCA](https://lorenagmad.github.io/tela_uca/) (Technology Enhanced Learning for All), Departamento de Ingeniería Informática, Campus de Jerez, Universidad de Cádiz.
