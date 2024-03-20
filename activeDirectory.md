# Configuración del servicio DNS

1. #### Objetivo:
  Configurar un servicio DNS en Windows Server 2019 o en un servidor Ubuntu con Docker,
  para el dominio ` lalaboral.local` y asignar direcciones IP a los equipos dentro del dominio.

  Los equipos dentro del dominio ` lalaboral.local` podrán resolver nombres de host y
  direccionamiento IP utilizando el servidor DNS configurado. 

  

  ##### a. Instalación del Servicio DNS 

![imagen](https://github.com/Musthit/TrabajoActive/assets/100193393/3e29ab93-5d05-4ba3-803b-51a7f71edffe)

  *Cambiamos la ip del servidor*

  *Cambiamos el nombre del equipo*

![imagen](https://github.com/Musthit/TrabajoActive/assets/100193393/44ba1648-d3c0-406b-91a3-8479298ffb95)

​	*Agregamos el Servidor DNS*

![image-20240319204235080](./assets/image-20240319204235080.png)

​	*Instalación en progreso*

![image-20240319204415389](./assets/image-20240319204415389.png)

​	*Terminada con éxito*

##### 	b. Configuración de Zonas y Registros DNS		

​	![image-20240319205054916](./assets/image-20240319205054916.png)

​	*Creamos la zona de búsqueda directa llamada `lalaboral.local`*



![imagen](https://github.com/Musthit/TrabajoActive/assets/100193393/d88c3135-3b27-4baf-ac7a-2a8807e8bd4c)

​	*Zonas creadas*



- Agregar registros A para los equipos creados en el ejercicio anterior, incluyendo el servidor:

  - server.lalaboral.local -> 172.17.10.10

![imagen](https://github.com/Musthit/TrabajoActive/assets/100193393/6517f640-b307-4db5-8330-be906b5a2ed4)

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

 ![imagen](https://github.com/Musthit/TrabajoActive/assets/100193393/11530a35-89c9-4a73-b968-0b7b46ca645c)

![imagen](https://github.com/Musthit/TrabajoActive/assets/100193393/ab54c9f7-9995-435c-9b53-a8c915f857c2)

  - Agregar registros PTR para asociar las direcciones IP con los nombres de host correspondientes.

 ![imagen](https://github.com/Musthit/TrabajoActive/assets/100193393/a94fbb95-6bfe-4a3d-8079-6f99be07a35e)


*VERIFICACIÓN*

![imagen](https://github.com/Musthit/TrabajoActive/assets/100193393/d8601137-0d4a-4237-98b5-fa7da8246a71)

*Ponemos la direccion ip dentro del rango 172.17.10.0 y el dns del server*

![imagen](https://github.com/Musthit/TrabajoActive/assets/100193393/00f03b08-fd5a-44f2-9c53-a0446867b725)

*Configuramos el archivo /etc/resolv.conf*

![imagen](https://github.com/Musthit/TrabajoActive/assets/100193393/d823a798-c03f-4158-ac2e-92b8b082f061)
*VERIFICACION CORRECTA*

