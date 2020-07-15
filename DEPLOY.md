# Plan de Implementacion: Openstack-dev MINSAL

Como prueba de concepto se realizara una implementacion de prueba, en 2 servidores fisicos.

OpenStack + Ceph + Ansible + Vagrant

Se instalara individualmente ceph (usando ansible) y luego se instalara y conectara OpenStack 
a la Instalacion de ceph.

Se utilizara como referencia:

Para OpenStack:
https://docs.openstack.org/project-deploy-guide/openstack-ansible/ussuri/overview.html
Version de OpenStack: Ussuri. Mayo 2020

Para Ceph:
https://docs.ceph.com/ceph-ansible/stable-5.0/
Version de Ceph: Octopus (15.2.3) May 2020


# Hardware:
  Listado de equipo para computo, almacenamiento y red disponible para la implementacion.

  deployment host: 
    Se utilizara una laptop fuera del segmento de red de los hosts fisicos, con la configuracion de la implementacion
    - alice (192.168.6.x) debian buster (10.4)

  target hosts:      
    - debianhost01 (10.10.20.40) debian buster (10.4)
    - debianhost02 (10.10.20.50) debian buster (10.4)
    Cada servidor contiene:
    - 4x CPUs AMD Opteron 6172 @2.1Ghz 12 cores (total 48 cores)
    - 64 GB RAM.
    - 2.7 TB HDD RAID5 (LVM)
    - 1.33 GB RAM / core

  Se utilizaran 2 hosts fisicos que simularan ser un rack.
    - rack001: debianhost01
    - rack002: debianhost02

  Se instanciaran X hosts virtuales (usando vagrant + virtuabox) en cada rack, simulando ser un host fisico.
    Openstack:
      - 1 control plane node
      - 2 compute node
      - 2 network node
    Ceph:
      - 2 mon node
      - 2 osd node 
      - 1 mgr node


# Direccionamiento de Red:
  Segmentos de Red
  Red de servidores fisicos:    10.10.20.0/24
  Red de administracion de VMs: 172.29.10.0/24
  Tuneles VxLAN (tenant?):     172.29.20.0/24
  Red de Almacenamiento (ceph): 172.29.30.0/24

  VLANs?

  Direcciones IP y MAC para los equipos.

# Configuraciones de Implementacion especificas:
  Ansible playbooks?
  ceph
  openstack

# Requerimientos:
  Configuracion de Hardware (iDrac?, BIOS?, etc)

  Configuracion de switches.

  LUN iscsi?




