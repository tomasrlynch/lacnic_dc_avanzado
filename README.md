# Servicios Avanzados de Data Centers - LACNIC
Para estos cursos, los laboratorios son generados automáticamente utilizando [netlab](https://netlab.tools/). Cada uno de los directorios de los laboratorios tiene un archivo `topology.yml` y configuraciones de soporte con extensión `.j2` que son utilizados por netlab para crear cada una de las topologías con las que trabajamos.
> [!NOTE]
> Las configuraciones de los hosts no se muestran debido a que hay muchas maneras distintas de configurarlos y en este curso son simples servidores Linux. En los laboratorios utilizaremos Alpine Linux ya que viene por defecto en netlab.

## Laboratorios 
El curso de Servicios Avanzados cuenta con seis laboratorios. El primero es de BGP para clientes y los restantes están basados en VXLAN y EVPN.

### Servicio de BGP
El laboratorio muestra las configuraciones necesarias en los Leaves y Hosts para dar un servicio de BGP a los clientes. Los componentes son:
- Dos routers de proveedores
- Dos routers de Borde
- Dos Spines
- Cuatro Leafs
- Cuatro Hosts

Con esta base se arman dos laboratorios muy parecidos pero que difieren en la configuración de los Hosts:
1. Servicio Básico de BGP en [Servicio BGP Simple](https://github.com/tomasrlynch/lacnic_dc_avanzado/tree/main/servicio_bgp_simple)
2. Servicio Anycast de BGP en [Servicio Anycast](https://github.com/tomasrlynch/lacnic_dc_avanzado/tree/main/servicio_anycast)

### Servicio de Redes Privadas Capa 2
El laboratorio muestra las configuraciones de VXLAN y EVPN para túneles de capa 2. Existen dos VXLAN distintas y estos son sus componentes:
- Cuatro hosts de VXLAN 101000 denominados `host[1-4]1`
- Cuatro hosts de VXLAN 101001 denominados `host[1-4]2`
- Dos hosts `host[AB]` que son clientes unicast IPv6
- Dos Spines
- Cuatro Leaves

Los archivos de configuración de este laboratorio se encuentran en [VXLAN Capa 2](https://github.com/tomasrlynch/lacnic_dc_avanzado/tree/main/vxlan_l2)

### Servicio de Redes Privadas Capa 3
El laboratorio muestra las configuraciones de VXLAN y EVPN para túneles de capa 3. Existen dos VXLAN distintas y estos son sus componentes:
- Cuatro hosts de VXLAN 10001 / VRF Azul denominados `host[1-4]1`
- Cuatro hosts de VXLAN 20002 / VRF Verde denominados `host[1-4]2`
- Dos hosts `host[AB]` que son clientes unicast IPv6
- Dos Spines
- Cuatro Leaves

Los archivos de configuración de este laboratorio se encuentran en [VXLAN Capa 3](https://github.com/tomasrlynch/lacnic_dc_avanzado/tree/main/vxlan_l3)

### Servicio de Conexión Externa
En este laboratorio se extiende el concepto de VXLAN capa 2 para dar servicios de conectividad externa. Para simplificar el laboratior solamente hay una VXLAN y los siguientes componentes:
- Un spine
- Dos leaves, uno dedicado a conectividad externa
- Un host conectado a la red de data center
- Un router y un host simulando una red remota en la oficina del cliente.

Los archivos de configuración de este laboratorio se encuentran en [Conexión Externa](https://github.com/tomasrlynch/lacnic_dc_avanzado/tree/main/conexion_externa)

### Interconexión de Data Centers (DCI)
El laboratorio de DCI simula dos data centers interconectados por sus routers de borde. Cada DC cuenta con:
- Un router de borde
- Dos spines
- Dos leaves
- Dos hosts

Los archivos de configuración de este laboratorio se encuentran en [DCI](https://github.com/tomasrlynch/lacnic_dc_avanzado/tree/main/dci)

### Interconexión de Data Centers (DCI) para Múltiples Data Centers
El laboratorio de DCI simula tres data centers interconectados por sus routers de borde. Cada DC cuenta con:
- Un router de borde
- Un spine
- Un leaf
- Un host

Los archivos de configuración de este laboratorio se encuentran en [DCI con Route Server](https://github.com/tomasrlynch/lacnic_dc_avanzado/tree/main/dci_rs)

## Configuraciones Finales
Las configuraciones finales de todos los laboratorios se encuentran en [configuraciones](https://github.com/tomasrlynch/lacnic_dc_avanzado/tree/main/configuraciones).
