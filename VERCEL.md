# Publicar Agenda Pro en Vercel: qué hace falta

Este repositorio contiene una aplicación **Electron de escritorio**, no una aplicación web lista para Vercel.

Vercel puede alojar frontends web, pero no ejecuta la ventana Electron, no proporciona notificaciones nativas de macOS y no ofrece una base SQLite local persistente (`better-sqlite3`) como lo hace el proceso principal de Electron.

## Arquitectura recomendada

- Mantener este proyecto Electron para escritorio/offline.
- Crear un frontend web compatible con navegador (React/Vite).
- Sustituir `window.agenda` e IPC por una capa de servicios web.
- Sustituir SQLite local por una base de datos gestionada (por ejemplo PostgreSQL) y almacenamiento de objetos para audios.
- Implementar autenticación y autorización antes de guardar datos personales.
- Usar notificaciones web; para avisos con la pestaña cerrada se requiere Web Push, service worker y backend programador.

## Configuración de Vercel para la futura versión web

- Framework preset: Vite
- Build command: `npm run build:web`
- Output directory: `dist`

**No despliegues este proyecto Electron directamente en Vercel**: el build actual no produce un sitio web autónomo y sus funciones principales dependen del proceso Electron.
