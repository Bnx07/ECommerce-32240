
# ECommerce-32240
## Aplicación web de Ecommerce de productos con logger y swagger implementado.

## Repositorio de todos los archivos y no solo el proyecto

 - [Repositorio general](https://github.com/Bnx07/CoderHouse-Backend-32240/)

## Instalación

Instalar ECommerce-32240 con git

```bash
  git clone https://github.com/Bnx07/ECommerce-32240.git
```

O instalar todo con

```bash
  git clone https://github.com/Bnx07/CoderHouse-Backend-32240.git
```

## Campos del .ENV

 - `PORT`
 - `CONNECTION` 
 - `BCRYPTGENSALT`
 - `JWTKEY`
 - `PERSISTENCE`
 - `MAILPASSWORD`
 - `LOGGER`

## Para ejecutar la aplicación

```bash
  npm install
  npm run dev
```

## Información del proyecto

El proyecto cuenta con varias APIs, las cuales son 
 - session
 - carts
 - products
 - tickets
 - messages

Para acceder a la documentación de las mismas, ejecute la apliación y vaya a

```http
/apidocs
```

## Tests

Para ejecutar los tests del servidor que conforman las rutas principales de las APIs session, products y carts, ejecute
 
```sh
npx mocha test/supertest.test.js
```

## Persistencias

El proyecto puede trabajar tanto con Mongo como con persistencia en archivos, esto se define en el PERSISTENCE del .env y utiliza el patrón Factory para alternar entre estos

## User Experience

La aplicación cuenta con varias secciones, incluyendo un chat para usuarios, un sistema de roles para la creación y modificación de archivos, usuarios con carritos autogenerados para cada usuario, sistema de compras con control y verificación de stock y motor de plantillas con handlebars. Los productos pueden ser agregados tanto por administradores como por usuarios premium; estos últimos pueden modificar y eliminar sus productos, pero no pueden añadirlos a sus carritos

## Usuario administrador

El usuario administrador tiene como email coderUser@coderhouse.com y como contraseña coderPassword

## Rutas de utilidad

Para conseguir 100 productos como si fuese una petición a MongoDB, ejecutar
```http
GET /api/products/mockProducts
```

Para arrojar un log de cada tipo
```http
GET /loggerTest
```

## Detalles

El programa arroja demasiados errores fatales por favicon y lectura de demás archivos

Para que los usuarios puedan pasar a ser premium, es necesario que suban sus documentos

Para que el servidor esté en producción y no muestre los loggers, el LOGGER del archivo .env debe ser "PRODUCTION"

## Relacionado

Para ver la documentación en inglés, lea

[README en inglés](https://github.com/Bnx07/CoderHouse-Backend-32240/)
