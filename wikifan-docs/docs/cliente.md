# Cliente

Sigue estos pasos para configurar y ejecutar el **cliente web de WikiFan**,
desarrollado con React y Vite.

!!! tip "Recomendación"
    Asegúrate de que el [Servidor (API)](servidor.md) esté en ejecución antes de
    iniciar el cliente, ya que la aplicación necesita comunicarse con él.

## 1. Ir a la carpeta del cliente

Si estás dentro de la carpeta `server`, regresa y entra a `client`:

```bash
cd ..
cd client
```

## 2. Instalar dependencias

=== "npm"

    ```bash
    npm install
    ```

=== "yarn"

    ```bash
    yarn install
    ```

## 3. Configurar la variable de entorno

Crea un archivo `.env` en la raíz del cliente y agrega la URL base de la API:

```bash
VITE_CORE_API_URL=http://localhost:3000
```

| Variable             | Descripción                                       |
| -------------------- | ------------------------------------------------- |
| `VITE_CORE_API_URL`  | URL base de la API con la que se comunica el cliente |

## 4. Iniciar el servidor de desarrollo

=== "npm"

    ```bash
    npm run dev
    ```

=== "yarn"

    ```bash
    yarn dev
    ```

La aplicación quedará disponible en `http://localhost:5173`.

¿Necesitas revisar la configuración del backend? Vuelve a la sección de
[Servidor (API)](servidor.md) o a la [página de inicio](index.md).
