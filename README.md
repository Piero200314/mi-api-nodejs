\# 🧩 Mi API Node.js



Backend inicial desarrollado con Node.js, Express, MySQL y Sequelize como parte de las prácticas de Fullstack en SENATI.



\## Alcance



Esta versión incluye:



\- Servidor Express.

\- Conexión a MySQL mediante variables de entorno.

\- Modelo de productos con Sequelize.

\- Sincronización de tablas.

\- Ruta de comprobación del servidor.



Las rutas CRUD y la autenticación JWT se desarrollan en el proyecto principal:

\[Inventario Fullstack](https://github.com/Piero200314/inventario-fullstack).



\## Tecnologías



| Tecnología | Uso |

|---|---|

| Node.js y Express | Servidor y API |

| MySQL y mysql2 | Persistencia de datos |

| Sequelize | Modelo y sincronización |

| dotenv | Configuración del entorno |

| cors | Acceso desde otros orígenes |

| nodemon | Reinicio en desarrollo |



\## Estructura



| Archivo | Función |

|---|---|

| index.js | Configuración y arranque |

| config/db.js | Conexión MySQL |

| models/Producto.js | Modelo de producto |

| package.json | Dependencias y comandos |

| .gitignore | Exclusión de archivos locales |



\## Instalación



Se necesita Git, Node.js, npm y MySQL en ejecución. Se puede utilizar Laragon para MySQL; Apache no es necesario.



```bash

git clone https://github.com/Piero200314/mi-api-nodejs.git

cd mi-api-nodejs

npm ci

```



\### Base de datos



Ejecuta en HeidiSQL o tu cliente MySQL:



```sql

CREATE DATABASE IF NOT EXISTS miapi\_db

CHARACTER SET utf8mb4

COLLATE utf8mb4\_unicode\_ci;

```



\### Variables de entorno



Crea `.env` en la raíz y adapta estos valores:



```dotenv

DB\_HOST=127.0.0.1

DB\_NAME=miapi\_db

DB\_USER=tu\_usuario

DB\_PASS=tu\_contrasena

PORT=3006

```



La conexión actual utiliza el puerto MySQL predeterminado 3306.



\### Ejecución



```bash

npm run dev

```



Para iniciar sin nodemon:



```bash

npm start

```



\## Comprobación



Abre http://localhost:3006/ después de que la terminal confirme la conexión.



| Método | Ruta | Respuesta |

|---|---|---|

| GET | / | ¡API Backend funcionando exitosamente! |



Esta versión todavía no expone endpoints para crear, listar, editar o eliminar productos.



\## Consideraciones



\- `.env` contiene configuración privada y no se publica.

\- `node\_modules` se instala mediante npm.

\- MySQL debe estar activo antes de iniciar.

\- No hay pruebas automatizadas configuradas.

\- No ejecutes esta API y otro backend en el mismo puerto.



\## Autor



\*\*Piero Huamani — SENATI\*\*  

Fullstack Developer Software - Seminario

