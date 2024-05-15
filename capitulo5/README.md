# Capítulo 5. Pruebas de carga y Rendimiento
## Carga y rendimiento en página web

## Objetivos
- Evaluar la capacidad, resistencia y estabilidad de una página web bajo condiciones de carga y demanda, así como analizar el rendimiento, eficiencia y tiempos de respuesta de la aplicación de calculadora en diferentes escenarios y cargas de trabajo.

### Duración aproximada: 40 minutos

## Instrucciones 
1. Abre **Apache JMeter**, con este se abrirá automáticamente en un plan de pruebas
    ![img](../images/capitulo5/img1.png)

2. **Añade un grupo de hilos**
    1. Da clic derecho sobre **Plan de pruebas** del menú de la izquierda.

    2. Selecciona: **Añadir**, **Hilos(usuarios)** y **Grupo de hilos.**
    ![img](../images/capitulo5/img2.png)

3. **Añade una petición HTTP**
    1. Da clic derecho sobre **Grupo de hilos.**
    2. Selecciona: **Añadir**, **Muestreador** y **Petición HTTP**.
    ![img](../images/capitulo5/img3.png)

4. **Configura la petición HTTP**
    1. Ingresa la información básica de: “**_Nombre de servidor_**” (URL): _iana.org_ y “**Ruta**”: _/domains_ Esto significa que se accederá a la página: iana.org/domains 
    ![img](../images/capitulo5/img4.png)

5. En un explorador abrimos el link _iana.org/domains_ para verificar el acceso y la información.
![img](../images/capitulo5/img5.png)


6. Hasta este momento, se ha añadido lo requerido para acceder a un link y realizar una prueba con cierta cantidad de usuarios (hilos), pero se requiere conocer los resultados. Para ello, se añaden receptores de información del link al que se desea someter a prueba.

    1. Da clic derecho sobre **Grupo de hilos**
    2. Selecciona **Añadir**, **Receptor** y **Ver Árbol de Resultados**
    ![img](../images/capitulo5/img6.png)

7. Se ejecuta la primera prueba, del acceso de un usuario por un segundo realizando este proceso una sola vez.
![img](../images/capitulo5/img7.png)

    1. Se solicita guardar el plan de pruebas antes de lanzarlo. Selecciona **Yes**
    ![img](../images/capitulo5/img8.png)

    2. Se guarda con el nombre: _ejemplo.jmx_ y seleccionamos **Save**.
    ![img](../images/capitulo5/img9.png)

    3. Revisa los resultados, seleccionado **Árbol de resultados.**
    4. Se mostrará una petición con resultado de muestreador y los datos de respuesta se mostrarán como el “código” del link al que se accedió. <br>
    ![img](../images/capitulo5/img10.png)
    ![img](../images/capitulo5/img11.png)


8. Selecciona en la pantalla de **Grupo de hilos**, el **Número de hilos** y aumenta a 350 y el período de subida (en segundos) a **10** y ejecuta nuevamente la prueba.<br>
    ![img](../images/capitulo5/img12.png)

    1. Revisa los resultados, seleccionando **Árbol de resultados.**
    2. Se mostrarán 350 peticiones con resultado de muestreador, y los datos de respuesta se mostrarán como el “código” del link al que se accedió.<br>
    ![img](../images/capitulo5/img13.png)

9. Cambia en la pantalla de **Grupo de hilos**, el período de subida (en segundos) a **90** y ejecuta nuevamente la prueba.
    ![img](../images/capitulo5/img14.png)

    1. Revisa los resultados, seleccionado **Árbol de resultados.**
    2. Se mostrarán 350 peticiones con resultado de muestreador, y los datos de respuesta se mostrarán como el “código” del link al que se accedió.<br>
    ![img](../images/capitulo5/img15.png)

10. Cambia en la pantalla de **Grupo de hilos**, el período de subida (en segundos) a **“1”** y ejecuta nuevamente la prueba.
    ![img](../images/capitulo5/img16.png)

    1. Revisa los resultados, seleccionado **Árbol de resultados.**
    2. Se mostrarán 350 peticiones con resultado de muestreador, y los datos de respuesta se mostrarán como el “código” del link al que se accedió. Debido a lo rápido y a la saturación de carga, es posible que algunas cargas sean erróneas.
    ![img](../images/capitulo5/img17.png)
    ![img](../images/capitulo5/img18.png)

11. **Añade otro receptor**
    1. Da clic derecho en el grupo de hilos.
    2. Selecciona: “añadir”, “Receptor” y “Gráfico de resultados”
    ![img](../images/capitulo5/img19.png)

12. Limpia los datos del **Árbol de resultados.**  Da clic derecho sobre **Árbol de resultados** y selecciona **Limpiar**. Los datos deberán eliminarse.
![img](../images/capitulo5/img20.png)


13. Realiza nuevamente pruebas validando el rendimiento de acuerdo con las variaciones de carga. Selecciona en la pantalla de **Grupo de hilos**, cambia el período de subida (en segundos) a **10** y ejecuta nuevamente la prueba.
    ![img](../images/capitulo5/img21.png)
    1. Revisa los resultados del **Árbol de resultados.** Se mostrarán 350 peticiones con resultado de muestreador, y los datos de respuesta se mostrarán como el “código” del link al que se accedió.
    ![img](../images/capitulo5/img22.png)

    2. Valida los resultados del **Gráfico de resultados.** Se mostrará una gráfica con el número de muestras, desviación, última muestra, rendimiento, media, mediana y los milisegundos en que se ejecutó.
    ![img](../images/capitulo5/img23.png)

14. Limpia los datos del **Árbol de resultados** y del **Gráfico de resultados**.  Da clic derecho sobre **Árbol de resultados** y selecciona **Limpiar**. Los datos deberán eliminarse.<br>
![img](../images/capitulo5/img24.png)


15. Selecciona en la pantalla de **Grupo de hilos**, cambia el período de subida (en segundos) a **120** y ejecuta nuevamente la prueba.
    ![img](../images/capitulo5/img25.png)

    1. Valida los resultados del **Gráfico de resultados**. Se mostrará una gráfica con el número de muestras, desviación,  muestra, rendimiento, media, mediana y los milisegundos en que se ejecutó.<br>
    ![img](../images/capitulo5/img26.png)

16. Limpia los datos del **Árbol de resultados** y del **Gráfico de resultados**.  Da clic derecho sobre **Árbol de resultados** y selecciona **Limpiar**. Los datos deberán eliminarse.
17. Selecciona en la pantalla de **Grupo de hilos** cambia el período de subida (en segundos) a **1** y ejecuta nuevamente la prueba.
    ![img](../images/capitulo5/img27.png)

    1. Valida los resultados del **Árbol de resultados**. Se mostrará una gráfica con el número de muestras, desviación,  muestra, rendimiento, media, mediana y los milisegundos en que se ejecutó.<br>
    ![img](../images/capitulo5/img28.png)

18. Valida que las tres graficas anteriores sean diferentes con sólo variar el período de subida, siendo que entre mayor sea el número de segundos, la página web se vuelve más estable.


### Solución o producto final
\#hilos: 350 // Periodo de subida:10<br>
![img](../images/capitulo5/img29.png)

\#hilos: 350 // Período de subida:120<br>
![img](../images/capitulo5/img30.png)

\#hilos: 350 // Período de subida:1<br>
![img](../images/capitulo5/img31.png)


