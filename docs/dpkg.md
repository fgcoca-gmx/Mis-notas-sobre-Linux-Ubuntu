***dpkg*** es el sistema de gestión de paquetes de bajo nivel para distribuciones de Linux basadas en Debian, como Ubuntu o Mint. 

Se utiliza directamente desde la terminal para instalar, eliminar, configurar y extraer información de archivos con extensión .deb.

## <FONT COLOR=#007575>**Características principales**</font>
* **herramienta de bajo nivel**: Opera directamente sobre los archivos .deb que ya tienes guardados en tu equipo.
* **Sin resolución de dependencias**: A diferencia de herramientas de nivel superior, dpkg no descarga ni resuelve automáticamente los programas o librerías adicionales que un paquete necesita para funcionar; si falta alguna dependencia, el proceso dará error.
* **Base de APT**: Herramientas más avanzadas y amigables para el usuario, como apt o apt-get, utilizan dpkg "en segundo plano" para realizar el trabajo de instalación real.

## <FONT COLOR=#007575>**Instalar paquete .deb**</font>
En sistemas con base Debian como Ubuntu, se pueden encontrar paquetes con la extensión .deb, y los mismos se pueden instalar desde la tienda de software, aunque para usuarios con conocimientos se suele emplear el comando ```sudo dpkg -i paquete.deb```.

Por ejemplo, instalamos el paquete ```abconnector_v6_0_linux64.deb```

```sh

sudo dpkg -i abconnector_v6_0_linux64.deb

```

## <FONT COLOR=#007575>**Desinstalar paquete .deb**</font>
Para mostrar la información del paquete basta con sustituir la bandera '-i' por 'f'.

```sh

sudo dpkg -f abconnector_v6_0_linux64.deb

```

Nos arroja un resultado como:

```sh
Package: abconnector
Architecture: all
Section: main
Maintainer: steamakersblocks@gmail.com
Priority: optional
Version: 6.0
Depends: python3,python3-tk,python3-serial,python-is-python3
Description: Connector v6.0
Homepage: https://www.steamakersblocks.com
```

Se muestra información del paquete como nombre del paquete, versión, arquitectura, etc.

Para desinstalarlo sólo quedaría usar la bandera 'r':

```sh

sudo dpkg -r abconnector_v6_0_linux64.deb

```

!!! Note "remove o purge"
    * ***dpkg -r / --remove***: Desinstala el programa, pero conserva los archivos de configuración en el sistema por si decides volver a instalarlo en el futuro.
    * ***dpkg -P / --purge***: Desinstala el programa y borra por completo todos los archivos asociados, incluidos los de configuración.
