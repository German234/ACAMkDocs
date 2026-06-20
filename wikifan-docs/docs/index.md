# WikiFan

![Logo de WikiFan](img/logo.png){ width="180" }

**WikiFan** es una API REST que permite consultar y administrar información
detallada sobre **series de televisión, películas, actores y personajes
ficticios**. Soporta operaciones CRUD completas (crear, leer, actualizar y
eliminar), autenticación de usuarios y una gestión de datos flexible.

El proyecto está formado por dos partes:

- **Servidor (API):** construido con Node.js, expone los endpoints y se conecta
  a una base de datos MongoDB.
- **Cliente:** una aplicación web desarrollada con React (Vite) que consume la API.

!!! note "Antes de empezar"
    Para ejecutar WikiFan necesitas tener instalados **Node.js 20 o superior**,
    **npm** o **yarn**, y **Git**. La configuración detallada se explica en cada
    sección.

## ¿Por dónde empezar?

- [Servidor (API)](servidor.md): instala y ejecuta el backend de WikiFan.
- [Cliente](cliente.md): levanta la aplicación web que consume la API.

Se recomienda configurar primero el servidor y luego el cliente.
