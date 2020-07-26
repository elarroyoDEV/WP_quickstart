# WP_quickstart Versión Adrián

## Quick start
- Poner los parámetros que se quieran en el fichero `config/.env.sample`
	- SITE_NAME="MI SITIO RÁPIDO"
	- SITE_ID="sitiorapido"
	- LOCALE=es_ES
	- DB_TABLE_PREFIX=wp_
- Abrir el composer.json y añadir los temas y plugins que se quieran de [wpackagist.org/](https://wpackagist.org/)
- Abri la consola e ir a la carpeta donde te has bajado el repositorio.
- Ejecutar desde consola `sh bin/setup`

- Si pones un fichero dump.sql en la carpeta dump, directamente te hará el import de ese fichero (recuerda de modificar el valor de DB_TABLE_PREFIX inicialmente para que concuerde con el del fichero)
	- Después tendrás que hacer un `lando wp search-replace 'http://urlviejadelabd' 'http://laurlquetehadadoelinstalador'`

## Posibles mejoras
- Hacer que te pregunte esos 3 campos del .env en un instalador y poder lanzar el instalador con este comando:
`git archive --remote=https://www.github.com/elarroyo/quickstart | tar -t | sh /bin/setup``

- Hacer que cuando se hace el import dump, pille el campo active_plugins de wp_options y haga un foreach instalando cada plugin.

- Preguntar en caso de que sea un import la URL vieja y forzar el wp search-replace

- ¿¿¿Hacer un merge para que todo esto se ejecute dentro del lando start???
