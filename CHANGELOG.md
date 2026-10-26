# Changelog

Formato basado en [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/).
Versionado: la serie pública actual es **0.x**; las versiones 1.0–1.3 corresponden a la
etapa con licencia (retirada) y se conservan solo como histórico.

## [0.9.0] — 2026-10-26

### Corregido
- **Restauración**: el filtro de rutas no coincidía con los patrones de restic, así que
  podía terminar con «0 archivos restaurados» sin avisar. Ahora convierte las rutas de
  Windows al formato de restic (`C:\Users\x` → `/C/Users/x`), admite varias rutas o
  patrones a la vez y muestra cuántos archivos se han recuperado.
- **Restauración**: los directorios restaurados podían quedar en solo lectura e impedir la
  escritura de los archivos. Se limpian esos atributos y se reintenta una vez.
- **Restauración**: los avisos de metadatos (fechas o permisos) ya no se tratan como fallo
  cuando los archivos sí se han restaurado.
- **Restauración al origen**: los archivos que no se pueden reubicar cuentan como error y
  la carpeta temporal no se borra, para no perder datos.
- **Tareas programadas**: ya no se borra la programación anterior antes de crear la nueva
  (si se cancelaba el aviso de permisos de Windows se quedaba sin nada). Se verifica que
  cada tarea existe y se muestra la próxima ejecución en la interfaz.
- **Tareas programadas**: la lectura del estado funciona en cualquier idioma de Windows.

### Añadido
- **Versión portable**: ZIP que se ejecuta sin instalar; perfiles, claves, registros y
  binarios se quedan en su propia carpeta. El título indica «(portable)».
- Nuevo comando `--rutas` para ver el modo y las carpetas en uso.

### Cambiado
- Numeración de versiones a **0.x** (antes 1.3.0). El instalador permite bajar de versión,
  así que actualizar desde la 1.3.0 funciona sin desinstalar.
- Retirado todo el código de licencias y el botón de importar licencia.

### Eliminado
- Comandos `--licencia` y `--generar-licencia`.

## [1.3.0] — 2026-10-22

### Cambiado
- El programa pasa a ser **gratuito**: todas las funciones desbloqueadas, sin licencia.
- Nuevo botón **Donar** en la cabecera.
- EULA reescrita para el modelo gratuito.

### Corregido
- Pestañas y desbordes de la interfaz principal.

## [1.2.0] — 2026-09

- Aviso de supervisión tras cada copia.

## [1.1.0] — 2026-09

- Multiperfil, presets y analizador de carpeta, cuatro tipos de destino, claves protegidas
  con DPAPI, programador con aviso y explorador de copias.

## [1.0.x] — 2026-09

- Serie inicial con licencia por PC.
