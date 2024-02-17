# WordPress con Docker Compose, Traefik y Memcached

Este proyecto facilita el despliegue de una instancia de WordPress utilizando Docker Compose, con MariaDB para la base de datos, Memcached para el almacenamiento en caché de objetos, y Traefik como proxy inverso para manejar el tráfico HTTPS.

## Requisitos Previos

- **Docker y Docker Compose**: Debes tener Docker y Docker Compose instalados en tu sistema.
- **Traefik Configurado**: Es necesario tener Traefik ya configurado y corriendo. La configuración de Traefik que uso la encontrarás en `/traefik`.
- **Portainer (Opcional)**: Si deseas utilizar Portainer para la gestión de contenedores, deberías tenerlo instalado y configurado.

## Configuración Inicial

### 1. Configuración de Traefik

Asegúrate de que Traefik esté configurado para manejar conexiones HTTPS y tenga habilitado un resolver para certificados SSL, como Let's Encrypt. La configuración específica de Traefik debe estar en tu carpeta `/traefik`.

### 2. Archivo de Variables de Entorno

Crea un archivo `.env` en el directorio raíz de este proyecto con las siguientes variables, ajustándolas según tu configuración:

```env
# -- INSTANCE CONF -- #
INSTANCE_NAME=my_site_instance
DOMAIN_HOST=mydomain.com
SUB_DOMAIN=subdomain

# -- WORDPRESS -- #
WORDPRESS_USERNAME=wp_user
WORDPRESS_PASSWORD=wp_password
WORDPRESS_EMAIL=wp@mail.com

# -- DATABASE -- #
MARIADB_PASSWORD=db_password
MARIADB_ROOT_PASSWORD=db_root_password
```

## Soporte y Contribuciones

Si tienes preguntas, problemas o sugerencias, no dudes en abrir un issue o un pull request en este repositorio.
