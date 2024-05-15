
# Capítulo 9. Pruebas en Entornos DevOps
## Calculadora VII

## Objetivos
Al finalizar la práctica, serás capaz de:
- Descubrir el uso de pruebas en entornos DevOps e integrar al ejercicio de calculadora.

### Duración aproximada: 45 minutos


## Instrucciones 

1. Accede a Azure DevOps
2. Agrega una nueva organización.
3. Ingresa el nombre dle proyecto: "_CalculadoraWeb_"<br>

    ![img](../images/capitulo9/img1.png)

4. Selecciona **Crear proyecto**<br>

    ![img](../images/capitulo9/img2.png)

5. Conecta Visual Studio a Git.
    1. Abre Visual Studio.
    2. Selecciona en el menú superior "**Git**" y "**Clonar repositorio**".
        ![img](../images/capitulo9/img3.png)

    3. Selecciona en **Examinar un repositorio Azure**

        ![img](../images/capitulo9/img4.png)
    
    4. Selecciona al que se añadió en DevOps. 
    5. Selecciona **Clonar**

        ![img](../images/capitulo9/img5.png)
    
    6. Solicitará la información para validar la cuenta. <br>
        ![img](../images/capitulo9/img6.png)
    
    7. El proyecto está clonado, selecciona la solución _CalculadoraWeb_
        1. Valida que se pueda acceder a la página web. Se mostrará la siguiente versión de la calculadora. 
            ![img](../images/capitulo9/img7.png)

6. Regresa a Azure DevOps. Se mostrará en Files la documentación correspondiente a la calculadora web.
    ![img](../images/capitulo9/img8.png)

7. Explora el área de repos.

8. Selecciona en el menú izquierdo **Boards** y **Boards**. En este apartado, encontrarás todas las actividades del equipo divididas en: Por hacer, haciendo y terminadas. <br>
    ![img](../images/capitulo9/img9.png)

    1. Añadiremos actividades
        - Selecciona **Añadir item**<br>
            ![img](../images/capitulo9/img10.png)

        - Añade los siguientes items:
            > - Calculadora web
            > - Lector de texto
            > - Traductor

            ![img](../images/capitulo9/img11.png)

        - Configura **Calculadora Web**
            - Selecciona **Calculadora web**<br>
            ![img](../images/capitulo9/img12.png)

            - Asígnate la actividad
            - Añade una descripción de la actividad
            - Coloca la prioridad 1.
            - Cierra y guarda.<br>
            ![img](../images/capitulo9/img13.png)

            - Lleva _Calculadora web_ a "**Doing**"<br>
            ![img](../images/capitulo9/img14.png)

    
    2. Agrega una prueba
        - Del menú de la izquierda, selecciona **Test plans**
        - Selecciona **New test plan**<br>
        ![img](../images/capitulo9/img15.png)

        - Ingresa el nombre de "_Pruebas unitarias_" y selecciona "**Crear**"<br>
        ![img](../images/capitulo9/img16.png)

        - Añade un **Nuevo caso de prueba**<br>
        ![img](../images/capitulo9/img17.png)

        - Ingresa el título "_Suma_"
        - Añade los pasos de la prueba de suma. <br>
        ![img](../images/capitulo9/img18.png)

        - Selecciona **Guardar** y modifica el estatus a **Listo**<br>
        ![img](../images/capitulo9/img19.png)

        - Selecciona **Guardar**
    
    3. Añadimos el caso de prueba a _Calculadora web_

        - Seleccionamos **Añadir link** y da clic en **Item existente**<br>
        ![img](../images/capitulo9/img20.png)

        - Selecciona **Test** a _Calculadora web_ y da clic en **Ok**<br>
         ![img](../images/capitulo9/img21.png)

        - Selecciona **Guardar y cerrar**
    
    4. Valida la información en **Boards**<br>
    ![img](../images/capitulo9/img22.png)

    5. Añade los casos de prueba de resta, multiplicación y división. 
  
### Solución o producto final
![final](../images/capitulo9/img23.png)


