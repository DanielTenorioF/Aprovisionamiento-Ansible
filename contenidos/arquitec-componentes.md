# Arquitectura y Componentes

## Arquitectura

Ansible utiliza una arquitectura basada en controladores y nodos para la administración de configuración. La máquina de control, donde comienza la orquestación, gestiona los nodos a través de SSH y los identifica mediante un inventario. Ansible despliega módulos temporalmente en los nodos a través de SSH, y estos módulos se comunican con la máquina de control mediante el protocolo JSON sobre una salida estándar. 

A diferencia de otros programas como Chef y Puppet, Ansible adopta una arquitectura sin agentes, eliminando la necesidad de instalar y ejecutar procesos de comunicación en los nodos. 

Esto reduce la sobrecarga de la red y evita estrategias de control agresivas por parte del servidor, como sondeos constantes.

![image](/img/23.jpg)

## Componentes

Los componentes principales de Ansible, a la hora de realizar el despliegue de aplicaciones, la orquestación multi-nivel y la gestión de la configuración, son los siguientes:

**Módulos:** Unidades de trabajo idempotentes que controlan servicios, ficheros o comandos, escritos en lenguajes como Python o Bash.

**Playbooks:** Archivos YAML que definen tareas y gestionan la configuración en un conjunto de hosts.

**Inventory:** Archivo donde se definen hosts y variables asociadas, como el puerto SSH.

**Roles:** Conjuntos de archivos y tareas para tipos específicos de hosts, simplificando la organización.

**Files:** Directorio para almacenar archivos a copiar en hosts asociados a un rol.

**Tasks:** Directorio donde se definen tareas a ejecutar en hosts específicos, cada una con un nombre descriptivo.

![image](/img/21.jpg)