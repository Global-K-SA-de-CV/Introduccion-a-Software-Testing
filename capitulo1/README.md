
# Nombre Laboratorio

Este texto es una descripción general del proyecto. Se debe de sustituir por el contenido
que el instructor decida agregar. 

## Objetivos
- objetivo1
- objetivo2
- objetivo3
- objetivo4


## Diagrama (Opcional / se puede cambiar por introducción)
Se espera que el alumno pueda implementar el siguiente contenido. 

![diagrama1](../images/img1.png)


## Instrucciones 
### Configuración de contenedor mysql
1. Crear una red con el siguiente comando
```shell
docker network create --subnet 10.0.0.0/16 --gateway 10.0.0.1 red2
```

2. Ahora crearemmos el contenedor del servidor virtual de mysql. 

- Usar el siguiente comando: 

```shell
docker run --name mysqlserver -e MYSQL_ROOT_PASSWORD=1234 -e MYSQL_DATABASE=traducciones --network mired -d mysql:8.0
```

- En el comando tenemos los siguientes datos:
    - User: root
    - Password: 1234
    - Database: traducciones
    - Network: mired
    - Name: mysqlserver 

> [!IMPORTANT]
> Recordar el nombre del contenedor ya que lo usaremos más adelante. 


### Configuración de contenedor backend y frontend
Para esta secciones necesitaremos el contenido de nuestro repositorio en la carpeta capitulo1

1. Descargar el archivo de la siguiente ruta
https://github.com/EdgardoVelasco/SeguridadApisCourse/tree/master/capitulo2

- En el repositorio encontraremos el siguiente contenido. 
![imagen repositorio](../images/img2.png)




### Resultado esperado
En esta sección se debe mostrar el resultado esperado de nuestro laboratorio
![imagen resultado](../images/img3.png)


