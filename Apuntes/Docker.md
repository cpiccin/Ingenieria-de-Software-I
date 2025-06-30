# Docker 

Docker es una herramienta que automatiza el despliegue de aplicaciones aisladas dentro de contenedores

Forma tradicional de desplegar una aplicación:
- Acceder directamente al sistema a configurar
- Copiar código/ejecutable a desplegar
- Usar herramientas interactivas para inspeccionar y modificar el sistema
- Asegurar que todas las dependencias estén presentes

Problemas
- Altamente repetitivo
- Gran probabilidad de error
- Interacciones entre aplicaciones
- Es difícil reconstruir la configuración ("Funciona en mi máquina staging")

### Configuracion de maquinas - Infrastructure as Code
En lugar de realizar modificaciones manualmente, se usa un lenguaje de programación, generalmente declarativo, específico para el dominio de configuraciones de máquinas (Ansible, Chef, Puppet, Terraform)

**Declarativo**: Especifica qué objetivo lograr </br>
**Imperativo**: Especifica cómo lograr el objetivo

![image](https://github.com/user-attachments/assets/c1349815-9132-4987-a4ae-0f6bfbf45dfc)


### Mascota vs Ganado
| Infraestructura Mascota                               | Infraestructura Ganado                                  |
|--------------------------------------------------------|----------------------------------------------------------|
| 🐕<br>- Nombres específicos<br>- Únicas<br>- Cuidadas   | 🐄🐄🐄🐄🐄<br>- Número de serie<br>- Prácticamente idénticas<br>- Reemplazable |
| - Mantenimiento delicado<br>- Presentes aunque no sean necesarios | - "Mantenimiento" creando otra instancia<br>- Se crean y destruyen a necesidad |
| - Servicios legacy<br>- Servicios únicos               | - Servicios sin estado interno relevante                 |


### Maquinas virtuales
Se emula un hardware por abajo del SO "invitado" que es gestionado por un hipervisor (monitor de máquina virtual) que a su vez corre en el sistema operativo que esta sobre su propio hardware

![image](https://github.com/user-attachments/assets/84fa917d-5e95-443b-8738-1a1949002395)

Emulación de una máquina real
- Provee aislamiento total
- Única opción para ejecutar programas de otras arquitecturas de hardware
- Al menos dos sistemas operativos ejecutando

Resulta ser algo lento porque es pesado correr x cantidad de sistemas operativos

### Linux Namespaces
Linux namespaces son una funcionalidad del kernel de Linux que permite aislar recursos del sistema entre procesos. Permiten que un proceso vea y utilice solo una parte de los recursos del sistema, como si fuera el único proceso en el sistema.

| Namespace | Aísla...                                      | Ejemplo en contenedores Docker                                |
|-----------|-----------------------------------------------|----------------------------------------------------------------|
| `pid`     | Procesos                                      | Cada contenedor tiene su propio árbol de procesos              |
| `mnt`     | Sistemas de archivos (mount points)           | Un contenedor tiene su propio sistema de archivos              |
| `net`     | Interfaces de red, IPs, puertos               | Cada contenedor puede tener su propia IP                       |
| `uts`     | Nombre del host y nombre de dominio           | Un contenedor puede tener su propio `hostname`                 |
| `ipc`     | Recursos de comunicación entre procesos       | Aísla colas de mensajes, semáforos, memoria compartida         |

## Contenedores
Linux Namespaces para separar grupos de procesos
- Aislamiento configurable entre aplicaciones
- Usan el mismo kernel que el host
- Overhead mínimo

![image](https://github.com/user-attachments/assets/871a3d46-da7e-4314-bb9d-01d0ebdb8742)

La idea es que en vez de estar trabajando con un segundo SO embebido en el primero, se hace que el mismo kernel del SO anfitrión aísle y gestione los recursos para cada contenedor, simulando entornos separados sin necesidad de virtualización completa.

## Docker
Conceptos: 
- Container: Grupo aislado de procesos
- Image: Template usado para crear contenedores (Sistema de archivos + metadata)
- Dockerfile: Archivo con instrucciones para construir una imagen

Brinda:
- Consistencia: Cualquier imagen se obtiene, inicia y configura de la misma manera
- Replicabilidad: Los contenedores basados en una misma imagen son inicialmente iguales
- Aislamiento: Se puede controlar la interacción entre la aplicación en un contenedor y el mundo exterior (en ambas direcciones)

![image](https://github.com/user-attachments/assets/3397207a-b306-4c89-8981-f7661662f5e6)

El usuario se comunica con el contenedor a traves de la aplicacion CLI de docker que tiene un cliente REST que se comunica con el servidor REST perteneciente al Docker Daemon

![image](https://github.com/user-attachments/assets/9476f4de-1d9d-4ffd-b363-7642481ed0f6)

