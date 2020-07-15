# Documento de Diseño.

# Antecendentes:
  Contamos con 50 servidores fisicos y 100 virtuales, que dia a dia se hace mas dificil su administracion.
  Necesitamos implementar una prueba de concepto (PoC) de nube privada para el MINSAL.

# Sumario:
  
# Requerimientos:
  Se requiere una plataforma de nube privada, con las siguientes caracteristicas:
  - Codigo abierto (Free Software).
  - Que se pueda usar con cualquier marca de servidores. (No hardware vendor lock-in)
  - Licenciamiento perpetuo (de preferencia gratuito).
  - Que brinde: Maquinas Virtuales, Contedores y Orquestacion de contenedores (Kubernetes).
  - Portal Web para Autoservicio (SelfService).
  - APIs, para usar con herramientas de automatizacion IaC (Infraestructura como Codigo). Terraform?

# Arquitectura Fisica:
  Descripcion de tipos de nodos
  Especificaciones Tecnicas de cada tipo de nodo
  Switches
  Gabinetes
  Conexiones intragabinete
  Conexiones intergabinete
  Conexiones electricas
  Topologia de Red

# Arquitectura de Servicio:
  Servicios y sus relaciones
  Diagrama

# Arquitectura de Inquilinos (tenant):
  Conpute Flavors.
  Images
  Arquitectura de identidad
  IPAM? 
  DDI?

# Roadmap:
  Versiones
  Futuras versiones y actualizaciones
  Modo de actualizacion

