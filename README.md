# Descripción del servicio

### Servicio 1: Recomendación de Donación <br />
La ONG a cargo del sistema quiere extender la posibilidad de donaciones a otras comunidades existentes. Para ello se requiere generar un servicio que dada una ubicación geográfica, propone los lugares dónde podés acercar donaciones.


## Guía completa y detallada de uso

- Paso 1: tener Node instalado [lo podes hacer en este link](https://nodejs.org/en/download/prebuilt-installer)
- Paso 2: tener MySQL server instalado
- Paso 3: clonar este repositorio en tu computadora
- Paso 4: abrir una consola parada en el proyecto y correr
  ``` npm i ``` Luego de este paso deberías tener una carpeta llamda `node_modules` en el proyecto
- Paso 5: configurar las variables de entorno: tenes que agregar a la raíz del proyecto un archivo con el nombre `.env` en el cual tenes que configurar las distintas credenciales de la base de datos. Acá tenes un ejemplo de como deberia quedar
``` env
DB_COMUNIDADES_USER=root
DB_COMUNIDADES_PORT=3306
DB_COMUNIDADES_PSWD=mysql
DB_COMUNIDADES_DBNAME=tp_dds_comunidades
DB_COMUNIDADES_HOST=localhost
```
Notar que antes de correr el servidor tenes que tener creada la base de datos vacía con el mismo nombre que está en `DB_COMUNIDADES_DBNAME` para que se pueda generar el esquema correctamente

- Paso 6: insertar algunos datos de prueba a la base de datos. Te dejamos este ejemplo, igualmente podes insertar lo que prefieras
 ``` sql
 INSERT INTO comunidad (id, nombre, lat, lon) VALUES
(1, 'Comunidad A', -34.61178, -58.417308),
(2, 'Comunidad B', -34.613466, -58.419659),
(3, 'Comunidad C', -34.582345, -58.43329),
(4, 'Comunidad D', -34.609897, -58.386682),
(5, 'Comunidad E', -34.630202, -58.471633),
(6, 'Comunidad F', -34.59868, -58.373928),
(7, 'Comunidad G', -34.617104, -58.362669),
(8, 'Comunidad H', -34.634981, -58.41324),
(9, 'Comunidad I', -34.609234, -58.445187),
(10, 'Comunidad J', -34.583449, -58.418373);
```
- Paso 7: una vez todo configurado ya podemos levantar el server ejecutando el siguiente comando en la terminal
  
   `npm run start`

- Si salió todo bien, ya podes empezar a usar el servicio! Para acceder a la documentación en local proba entrando a este link: http://localhost:3000/docs/

Tené cuidado! Para poder solicitar comunidades primero tenes que generar una API Key y ponerla en Headers: Authorization <br />
Si estás hace mas de 5 minutos y no te funciona, nos podes contactar! Abz.


