# Documento de Diseño.

# Antecendentes:
El centro de datos actual cuenta con 50 servidores fisicos y 100 virtuales, el provisionamiento es totalmente manual.
Se tiene la necesidad de crecer, para ello se implementara una prueba de concepto (PoC) de nube privada.

# Sumario:
  
# Requerimientos:
Se requiere una plataforma de nube privada, con las siguientes caracteristicas:
* Codigo abierto (Free Software).
* Que se pueda usar con cualquier marca de servidores. (No hardware vendor lock-in)
* Licenciamiento perpetuo (de preferencia gratuito).
* Que brinde: Maquinas Virtuales, Contedores y Orquestacion de contenedores (Kubernetes).
* Portal Web para Autoservicio (SelfService).
* APIs, para usar con herramientas de automatizacion IaC (Infraestructura como Codigo). Terraform?
* Modulo de facturacion (billing).
* Alamacenamiento (Bloque, Objetos, Ficheros).
* Hiperconvergencia (HCI) ?


# Matriz de Opciones

Caracteristicas | Xen | OpenStack | VMWare | Nutanix | Red Hat OpenStack
--- | --- | --- | --- | --- | --
Implementacion |Ya se tiene experiencia|inhouse (investigar)| 3 meses |3 meses?| 4 meses
Administracion | Aislada, CLI | Centralizada, Web, API | Centralizada, Web, API? | Centralizada, Web, API?, CLI? | Centralizada, Web, API
Soporte | inhouse | inhouse | Portal | Portal | Portal
Ciclo de Vida | inhouse | inhouse | Bajo Soporte | Bajo Soporte | Bajo Soporte
Flexibilidad | poca | mucha | poca | poca| media
Licencia | libre | libre | subscripcion | subscripcion | subscripcion
Costo | solo HW | solo HW | $?| $?| $?
Proveedor Local | no | no | RAF, TECNASA | TECNASA | RedSoft (DATUM)
Hardware | cualquiera | cualquiera | DellEMC VxRail/VRealize | DellEMC HC| cualquiera?



# Arquitectura Fisica:
## Descripcion de tipos de nodos
## Especificaciones Tecnicas de cada tipo de nodo
## Switches
## Gabinetes
## Conexiones intragabinete
## Conexiones intergabinete
## Conexiones electricas
## Topologia de Red

# Arquitectura de Servicio:
## Servicios y sus relaciones
## Diagrama

# Arquitectura de Inquilinos (tenant):
## Conpute Flavors.
## Images
## Arquitectura de identidad
### IPAM? 
### DDI?

# Roadmap:
## Versiones
## Implementacion
## Futuras versiones y actualizaciones
## Actualizacion (update)
## Upgrade 

