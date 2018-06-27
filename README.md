# IncidentManagementSystem
Sistema de gestión de incidencias. Está formado por cuatro módulos: dos de ellos (Loader y Agents) resuelven la gestión de usuarios y los otros dos (InciManager e InciDashboard) resuelven la gestión de incidencias.

A continuación se resume que hace cada uno, aunque se puede ver su información detallada en la página específica de cada uno de ellos:
 - [Loader](https://github.com/TaniaAlvarezDiaz/Loader): módulo para cargar los datos de los agentes que podrán enviar incidencias al sistema.
 - [Agents](https://github.com/TaniaAlvarezDiaz/Agents): módulo que permite a los agentes consultar y obtener información del sistema.
 - [InciManager](https://github.com/TaniaAlvarezDiaz/InciManager): módulo encargado de tramitar las incidencias que serán eviadas por los agentes. Dichos agentes deberán estar dados de alta en el sistema y tener permisos para enviar las incidencias.
 - [InciDashboard](https://github.com/TaniaAlvarezDiaz/InciDashboard): módulo que representa un cuadro de mandos, el cual permite al personal de gestión de incidencia poder visualizar y gestionar las incidencias que ocurren en el sistema.

# Author
Tania Álvarez Díaz ([@TaniaAlvarezDiaz](https://github.com/TaniaAlvarezDiaz))

# Execute

Para ejecutar el proyecto seguir los siguientes pasos:

1. Descargar el proyecto:
   * git clone
   * git submodule init
   * git submodule update

2. Importar el proyecto en Eclipse, STS, etc. como Maven Proyect si se desea ejecutar desde el IDE. En este caso, los puntos 5 y 6 se sustituirian por ejecutar desde el IDE el proyecto correspondiente.

3. Descargar [Apache Kafka](https://kafka.apache.org/quickstart) y seguir los siguientes pasos, todos ellos desde la consola CMD.
   * Ir a la capeta donde está el zip de Kafka descomprimido.
   * Ejecutar Apache Zookeeper. Para ello ejecutar:
     * En Windows: bin\windows\zookeeper-server-start.bat config\zookeeper.properties
     * En Mac: bin/zookeeper-server-start.sh config/zookeeper.properties
   * Se va a quedar bloqueada esa consola CMD, por tanto, sin cerrarla, abrir otra consola. Ejecutar Apache Kafka:
     * En Windows: bin\windows\kafka-server-start.bat config\server.properties
     * En Mac: bin/kafka-server-start.sh config/server.properties

4. Ejecutar la base de datos, en este caso HSQLDB, se encuentra en el submodulo "BaseDeDatos" de este proyecto.
   * Ir a la carpeta "bin"
   * Pulsar doble click sobre "runServer.bat"

5. Desde la carpeta InciManager ejecutar:
   * mvn spring-boot:run

6. Desde la carpeta InciDashboard ejecutar:
   * mvn spring-boot:run
   
7. Desde un navegador acceder a:
   * http://localhost:8091 para acceder al InciManager
   * http://localhost:8092 para acceder al InciDashboard

