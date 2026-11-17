# Agenda & Recordatorios Pro

Aplicación de escritorio offline para productividad y organización personal, construida con Electron, React, Vite, TypeScript, Tailwind CSS y SQLite local.

> **Importante sobre Vercel:** este repositorio contiene la aplicación Electron. Vercel no ejecuta aplicaciones Electron ni procesos nativos persistentes como `better-sqlite3` en su hosting web/serverless. Para publicar una versión web accesible desde el navegador hace falta una adaptación web separada con API, base de datos y almacenamiento compatibles con la nube.

## Requisitos

- Node.js 20 LTS o superior.
- macOS, Windows o Linux para desarrollo.

## Ejecutar en macOS

1. Descarga y descomprime el código fuente.
2. Abre Terminal en la carpeta del proyecto.
3. Ejecuta `npm install`.
4. Ejecuta `npm run dev`.

También puedes abrir `INICIAR-MAC.command`. La primera instalación necesita Internet para descargar dependencias; la aplicación y sus datos locales funcionan offline después.

## Scripts

- `npm run dev`: inicia Electron en desarrollo.
- `npm run build`: compila los procesos Electron y la interfaz.
- `npm run typecheck`: comprueba TypeScript.
- `npm run package`: genera instaladores con electron-builder.

## Funciones

- Dashboard y resumen diario.
- Calendario y citas.
- Recordatorios y contactos/cumpleaños.
- Programación de sesiones de grabación con fecha y hora.
- Biblioteca local de notas de voz.
- Notificaciones nativas mientras la aplicación permanece ejecutándose.

## Datos y privacidad

SQLite y los archivos de audio se almacenan localmente en el equipo. No se envían a servidores.

## Vercel

Consulta [VERCEL.md](./VERCEL.md) antes de intentar un despliegue web. No configures el proyecto Electron tal cual en Vercel: no funcionará como aplicación web.
