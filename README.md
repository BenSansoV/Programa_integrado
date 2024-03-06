Proyecto de integración de MySQL, Python y Power BI

El proyecto consiste en crear un database en tiempo real, la cual se irá alimentando de información que añadiremos con Python, para luego mostrar la información obtenida a través de un Dashboard en MS Power BI.
La información que brindaremos será la información de capacidad, memoria y rendimiento de tu computadora, que obtendremos a través de la librería 'psutil' de Python.


Pasos:
En MySQL:
1) Crear el Schema system_information
2) Crear la tabla performance, con la siguiente información:
    CREATE TABLE Performance (
    timestamp TIMESTAMP,
    cpu_usage FLOAT,
    memory_usage BIGINT,
    cpu_interrupts BIGINT,
    cpu_calls BIGINT,
    memory_used BIGINT,
    memory_free BIGINT,
    bytes_sent BIGINT,
    bytes_received BIGINT,
    disk_usage FLOAT
    );

En Python:
1) Importar las librerías mysql.connector, psutil y time
2) Establecer la conexión a MySQL. Debes entregar el host, user, password, database y port.
   Esta información la puedes obtener en la pestaña Session, que se encuentra ubicada abajo a la izquierda.
   La única información que no saldrá es la contraseña, por lo que deberás tenerla a mano o recordarla.
3) Establecer el ciclo while en tiempo real para obtener la información que necesitaremos.
   Considerar que será una ejecución manual, por lo tanto debes preocuparte de correr el script y también deberás detenerlo cuando estimes conveniente.
   Idealmente deja pasar unos minutos para poder tener una buena cantidad de información.

En Power BI
1) Abrir un archivo nuevo de Power BI
2) Ir a la pestaña Inicio, pinchar en Obtener datos para establecer una conexión con MySQL. En caso que te pida un conector, deberás descargarlo.
3) Establecer la conexión en MySQL, ingresando algunas de las credenciales entregadas en el script de Python.
4) Una vez conectado, se generan tres campos calculados en función del tiempo. Este dashboard es totalmente a elección del usuario.

Importante:
Puedes ejecutar el script de Python cuando desees para generar más información. Sin embargo, no se visualizará en el Dashboard de Power BI a menos que ejecutes la consulta de selección en MySQL.
