# Plan de Implementacion de Nube privada (Openstack + Ceph)

Como prueba de concepto (PoC), se realizara una implementacion en 2 servidores fisicos.

* node01
* node02

Se utilizaran las siguientes aplicaciones:
* OpenStack 
* Ceph 
* Ansible 
* Vagrant

Se instalara individualmente ceph (usando ansible) y luego se instalara y conectara OpenStack a la Instalacion de ceph.

Se utilizara como referencia:

## OpenStack
https://docs.openstack.org/project-deploy-guide/openstack-ansible/ussuri/overview.html

Version de OpenStack: Ussuri. Mayo 2020

## Ceph
https://docs.ceph.com/ceph-ansible/stable-5.0/

Version de Ceph: Octopus (15.2.3) May 2020


# Hardware:

Listado de equipo para computo, almacenamiento y red disponible para la implementacion.

## Deployment host: 

Se utilizara una laptop fuera del segmento de red de los hosts fisicos, con la configuracion de la implementacion

* laptop (192.168.6.x) debian buster (10.4)

## Target host:      
Se utilizaran 2 hosts fisicos que simularan ser un rack.

* node01 (10.10.20.40) debian buster (10.4)
* node02 (10.10.20.50) debian buster (10.4)

Cada servidor contiene:
* 4x CPUs AMD Opteron 6172 @2.1Ghz 12 cores (total 48 cores)
* 64 GB RAM.
* 2.7 TB HDD RAID5 (LVM)
* 1:1 GB RAM / core


Se instanciaran 10 hosts virtuales (usando vagrant + virtuabox) en cada nodo, simulando ser un host fisico.
## Openstack
* 1 control plane node
* 2 compute node
* 2 network node

## Ceph
* 2 mon node
* 2 osd node 
* 1 mgr node


# Direccionamiento de Red:
Red | nombre | segmento
----|--------|--------
Nodos (servidores fisicos) | undernetwork | 10.10.20.0/24
Administracion de VMs | netadmin | 172.29.10.0/24
Tuneles VxLAN (tenant?) | nettenant | 172.29.20.0/24
Almacenamiento (ceph) | netstorage |172.29.30.0/24

##  Creacion de redes mediante script: 
scripts/set-vxlans-physical-hosts.txt

  
## VLANs?

## Direcciones IP y MAC para los equipos.



# Configuraciones de Implementacion especificas:
## Ansible playbooks?
## ceph
## openstack

# Requerimientos:
## Configuracion de Hardware (iDrac?, BIOS?, UEFI?, PXE, etc)
## Configuracion de switches.
## LUN iscsi?
