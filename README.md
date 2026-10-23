# Densha de Go! Professional Shiyou — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/playstation/densha-de-go-professional)**.

Traducción al **español de España** de *Densha de Go! Professional Shiyou*
(電車でGO! プロフェッショナル仕様, PlayStation, 1999), el simulador de conducción de trenes
de Taito, que nunca salió de Japón.

La traducción se distribuye como **parche**. No incluye el juego: necesitas tu propia copia
japonesa para aplicarlo.

## Estado

Última versión: **[v1.0](../../releases/tag/v1.0)**, la primera.

| Parte | Estado |
|---|---|
| Cinta de avisos (selección de línea, horarios, museo, ajustes) | Traducida: descripciones de las 10 líneas y anuncios de los 75 servicios |
| Cartel «Próxima salida» (tren, destino, serie y paradas) | Traducido; las horas se quedan como en el original |
| Museo del Ferrocarril (fotos, modelos, vídeos, música) | Descripciones y lista de trenes traducidas |
| Ajustes, tarjeta de memoria y PocketStation | Traducidos |
| Texto dentro de imágenes (menús, horarios, marcador, guía, señales, avisos, fichas de los trenes, evaluación) | **1.235 rótulos redibujados** |
| Nombres de estación | En alfabeto latino (Hepburn) en horarios, mapas, marcador y carteles |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿ « »** |
| Revisión durante una partida | Parcial (ver abajo) |

Detalles:

- El juego dibujaba el texto con la fuente japonesa de la BIOS, que no tiene tildes ni eñes.
  El parche lleva una fuente nueva de ancho variable, sacada de esa misma fuente, con el mismo
  alto, trazo y colores, también en la matriz de puntos de la cinta de avisos.
- Los mensajes de la guía, las señales, los avisos de penalización y las fichas de los 90 trenes
  se han redibujado con letras del mismo color, borde y sombra que el original.
- Los nombres de estación siguen la romanización Hepburn sin macrones (Omagari, Kakunodate,
  Shin-Osaka), con Tokio y Kioto en su forma española. Se conservan los nombres de 1999.
- Los subtítulos en inglés de los menús («A Duty Of Driving Train»…) se conservan, igual que el
  logotipo.

Se quedan en japonés, porque no hay sitio en la imagen o el juego los lee de forma que no se
pueden redibujar sin romper otra cosa:

- El diagrama del mando en Ajustes, la cabecera «今度の発車は» del cartel de salida y la tira de
  estaciones que la acompaña en algunas líneas.
- Algunos carteles de andén (Kagoshima, y ocho estaciones de Yamanote y Keihin-Tohoku), el mapa de
  la línea circular de Osaka y unos pocos rótulos del paisaje.
- Los sellos de nota de la evaluación (秀 優 良 可) y los nombres del equipo en los créditos.
- Los pies de las fotos del museo, que forman parte de cada fotografía, y la voz y los rótulos de
  los vídeos.

### Comprobaciones y trabajo pendiente

Se ha jugado en emulador, siempre desde partida nueva, en cuatro rondas con candidatas sucesivas
(algo más de dos horas de juego en total). La versión publicada se ha jugado en el menú, los ajustes, el
museo, Cargar/Guardar y las líneas de Akita, Keihin-Tohoku norte, Hokuhoku y Sagano; el resto se
comprobó en candidatas anteriores con las mismas traducciones:

- **Conducción** en las diez líneas del menú, con horario, cartel de salida, ficha del tren,
  mensajes de la guía, señales, avisos de penalización, pausa, tiempo agotado, continuar,
  GAME OVER, evaluación y registro de servicio. Keihin-Tohoku sentido sur se ha jugado hasta el final.
- **Menús**: título, demostración, todos los ajustes, guardar, sobrescribir, cargar, formatear
  (comprobando que «No» no formatea), autoguardado, carga automática al arrancar y los avisos de
  PocketStation (sin PocketStation conectada).
- **Museo**: las cuatro salas, todas las regiones, el visor 3D, el pase de diapositivas y la
  sala de música.

Una auditoría automática comprueba en cada versión la posición de cada archivo en el disco, sus
sumas de control y los límites de memoria de cada módulo, y otra comprueba las listas de piezas
de los gráficos del marcador. El parche se ha aplicado sobre el BIN japonés original y el
resultado se ha comparado byte a byte con la imagen probada.

**No se ha jugado ningún recorrido completo con paradas correctas** ni se ha probado en consola
real: en las pruebas no se ha llegado a parar en el sitio en una estación, ni a los finales, los
créditos, la entrada de nombre ni el juego de bonificación. La traducción y su revisión se han
hecho con asistencia de IA, sin revisores humanos independientes. Si encuentras un error, abre
una incidencia con una captura.

Limitaciones conocidas:

- En los carteles de salida algunos destinos y nombres de tren van abreviados («Exp. lim.»,
  «Kanku», «temp.») porque el campo es estrecho.
- Algunos rótulos van muy apretados: el «no para» de los carteles de estación sobre la vía es
  pequeño, la cabecera «Línea principal San'in» va muy condensada y en Ajustes «Velocímetro» queda
  pegado a su valor.
- Al continuar tras agotar el tiempo, el rótulo «Reanude» sale cortado y más oscuro que el original.
- Los estados guardados del emulador (savestates) no sirven entre versiones del parche: usa la
  tarjeta de memoria del juego.

## Cambios

- **v1.0** (24-10-2026): primera versión.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia de **Densha de Go! Professional Shiyou (Japón)**, SLPM-86378, en formato
   BIN/CUE de una sola pista.
3. **Comprueba que tu copia es la correcta** antes de nada:

   | | |
   |---|---|
   | Archivo | `Densha de Go! Professional Shiyou (Japan).bin` |
   | Tamaño | 748.921.488 bytes |
   | MD5 | `4e487c1fa9f4e2b886ff24c0ab977606` |

   ```bash
   md5sum "Densha de Go! Professional Shiyou (Japan).bin"            # Linux
   md5 "Densha de Go! Professional Shiyou (Japan).bin"               # macOS
   CertUtil -hashfile "Densha de Go! Professional Shiyou (Japan).bin" MD5   # Windows
   ```

   Si no coincide, el parche fallará o dará un resultado corrupto.
4. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "original.bin" parche.xdelta "Densha de Go Professional (ES).bin"`
5. Comprueba que el BIN resultante tiene el MD5 **`8ffc7d98f643cace6c765b07525d6483`** (v1.0)
   y el mismo tamaño que el original.
6. Crea un CUE para el nuevo BIN, por ejemplo `Densha de Go Professional (ES).cue`:

   ```
   FILE "Densha de Go Professional (ES).bin" BINARY
     TRACK 01 MODE2/2352
       INDEX 01 00:00:00
   ```

7. Carga el CUE en tu emulador.

Aplica el parche sobre el **BIN japonés original**, no sobre una copia ya parcheada.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin relación alguna
con Taito ni Sony. Aquí no se distribuye el juego ni ninguna parte de él: solo un parche que
modifica una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia y lo hago.
