# Servidor (API)

En esta sección configurarás y ejecutarás el **servidor de WikiFan** en tu
máquina local.

## Requisitos previos

Asegúrate de tener instalado el siguiente software antes de comenzar:

| Software | Versión recomendada | Descripción                          |
| -------- | ------------------- | ------------------------------------ |
| Node.js  | 20.x o superior     | Entorno de ejecución de JavaScript   |
| npm      | 9.x o superior      | Gestor de paquetes (incluido en Node)|
| yarn     | 1.22.x o superior   | Gestor de paquetes alternativo       |
| Git      | Última versión      | Necesario para clonar el repositorio |
| MongoDB  | —                   | Base de datos del proyecto           |

## 1. Clonar el repositorio

```bash
git clone https://github.com/German234/WikiFan.git
cd WikiFan
cd server
```

## 2. Instalar dependencias

Usa tu gestor de paquetes preferido:

=== "npm"

    ```bash
    npm install
    ```

=== "yarn"

    ```bash
    yarn install
    ```

## 3. Configurar variables de entorno

Crea un archivo `.env` en la raíz del servidor con los siguientes valores:

```bash
PORT=3000
MONGO_URI=tu_url_de_base_de_datos
JWT_SECRET=tu_clave_secreta_jwt
```

| Variable     | Descripción                                          |
| ------------ | ---------------------------------------------------- |
| `PORT`       | Puerto donde se ejecuta el servidor (por defecto 3000)|
| `MONGO_URI`  | URL de conexión a tu base de datos MongoDB           |
| `JWT_SECRET` | Clave secreta para la autenticación con JWT          |

Puedes generar una clave aleatoria para `JWT_SECRET` con:

```bash
node -e "console.log(require('crypto').randomBytes(32).toString('hex'))"
```

!!! warning "Protege tus credenciales"
    Nunca subas el archivo `.env` al repositorio. Agrégalo a tu `.gitignore`
    para evitar exponer tu `MONGO_URI` y tu `JWT_SECRET`.

## 4. Iniciar el servidor

=== "npm"

    ```bash
    npm start
    ```

=== "yarn"

    ```bash
    yarn start
    ```

La API quedará disponible en `http://localhost:3000` (o el puerto que hayas
configurado). En esa misma dirección encontrarás la documentación de cada
endpoint.

Cuando el servidor esté funcionando, continúa con la configuración del
[Cliente](cliente.md).
