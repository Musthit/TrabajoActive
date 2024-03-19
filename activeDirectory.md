# Configuración del servicio DNS

1. #### Objetivo:
  Configurar un servicio DNS en Windows Server 2019 o en un servidor Ubuntu con Docker,
  para el dominio ` lalaboral.local` y asignar direcciones IP a los equipos dentro del dominio.

  Los equipos dentro del dominio ` lalaboral.local` podrán resolver nombres de host y
  direccionamiento IP utilizando el servidor DNS configurado. 

  

  ##### a. Instalación del Servicio DNS 

  ![image-20240319203450720](./assets/image-20240319203450720.png)

  *Cambiamos la ip del servidor*

  ![image-20240319203718201](./assets/image-20240319203718201.png)

  *Cambiamos el nombre del equipo*

  *(En este caso me cambió el nombre a SERVERVICTORDES porque el que puse es muy largo)*

  ![image-20240319204059885](./assets/image-20240319204059885.png)

​	*Agregamos el Servidor DNS*

![image-20240319204235080](./assets/image-20240319204235080.png)

​	*Instalación en progreso*

![image-20240319204415389](./assets/image-20240319204415389.png)

​	*Terminada con éxito*

##### 	b. Configuración de Zonas y Registros DNS

​		

​	![image-20240319205054916](./assets/image-20240319205054916.png)

​	*Creamos la zona de búsqueda directa llamada `lalaboral.local`*



![image-20240319205328155](./assets/image-20240319205328155.png)

​	*Creamos la zona de búsqueda inversa*

![image-20240319205422486](./assets/image-20240319205422486.png)

​	*Zonas creadas*



- Agregar registros A para los equipos creados en el ejercicio anterior, incluyendo el servidor:

  - server.lalaboral.local -> 172.17.10.10

    ![image-20240319210247061](./assets/image-20240319210247061.png)

  - Equipo_Ventas1.lalaboral.local -> 172.17.10.11

    ![image-20240319210728375](./assets/image-20240319210728375.png)

  - Equipo_Ventas2.lalaboral.local -> 172.17.10.12

    ![image-20240319210816930](./assets/image-20240319210816930.png)

  - Equipo_Marketing1.lalaboral.local -> 172.17.10.13

    ![image-20240319210909780](./assets/image-20240319210909780.png)

  - Equipo_Marketing2.lalaboral.local -> 172.17.10.14

    ![image-20240319210951692](./assets/image-20240319210951692.png)

  - Equipo_Operaciones1.lalaboral.local -> 172.17.10.15

    ![image-20240319211033406](./assets/image-20240319211033406.png)

  - Equipo_Operaciones2.lalaboral.local -> 172.17.10.16

    ![image-20240319211111045](./assets/image-20240319211111045.png)

- c. Configuración de Zona Inversa:

  - Crear una nueva zona de búsqueda inversa para la red 172.17.10.0.

    ![image-20240319211613338](./assets/image-20240319211613338.png)

    *Nueva zona de busqueda inversa creada*

  - Agregar registros PTR para asociar las direcciones IP con los nombres de host correspondientes.

    ![image-20240319211920782](./assets/image-20240319211920782.png)

    ![image-20240319211955662](./assets/image-20240319211955662.png)

    

*VERIFICACIÓN*

no va

![image-20240319234937387](./assets/image-20240319234937387.png)
