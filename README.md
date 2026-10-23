# AndreuMatic Backup — descargas

Repositorio **solo de binarios**. Aquí se publican los instaladores oficiales de
[AndreuMatic Backup](https://ambackup.andreumatic.com) y sus sumas de verificación.
El código fuente es privado.

## Última versión: 1.3.0

| Archivo | SHA-256 |
|---|---|
| `AMBackup-1.3.0.msi` | `CF69DFA1E062D558276C10221427485866D7B5A227C85FBC190FE29D7E2C6928` |

Descarga directa:
https://github.com/andreumatic/ambackup-releases/releases/download/v1.3.0/AMBackup-1.3.0.msi

Verificar en Windows:

```powershell
certutil -hashfile AMBackup-1.3.0.msi SHA256
```

Cada release incluye `SHA256SUMS.txt` con las sumas de todos sus archivos.

## Requisitos

Windows 10 (1809+) o Windows 11, 64 bits, 150 MB libres. Restic va incluido.

## SmartScreen

El instalador no usa certificado comercial: Windows puede avisar. Pulsa
**Más información → Ejecutar de todas formas** y comprueba antes el SHA-256.

## Documentación

- Web: https://ambackup.andreumatic.com
- Guía: https://ambackup.andreumatic.com/guia.html
- Descargas: https://ambackup.andreumatic.com/descargas.html
