### Eaton UPS Grafana Dashboard - SNMP v3

Os dejo por aquí los archivos de configuración necesarios para monitorizar vuestro UPS Eaton con Grafana con SNMPv3, con el que tendréis un panel como el que os muestro a continuación.

[![](https://www.edudima.com/wp-content/uploads/2024/01/1.jpg)](https://www.edudima.com/wp-content/uploads/2024/01/1.jpg)

Con este panel tendréis información relativa a los watts de salida, tiempo de backup en base a vuestras baterías y elementos conectados a ellas, estado de las baterías, voltaje y frecuencias de entrada y salida.

##### 1. Descarga MIBS

`usr/share/snmp/mibs`

Aseguraos tambien que vuestro archivo SNMP.conf se encuentra de la siguiente manera:

    # As the snmp packages come without MIB files due to license reasons, loading
    # of MIBs is disabled by default. If you added the MIBs you can reenable
    # loading them by commenting out the following line.
    mibs +ALL
    
    # If you want to globally change where snmp libraries, commands and daemons
    # look for MIBS, change the line below. Note you can set this for individual
    # tools with the -M option or MIBDIRS environment variable.
    #
    # mibdirs /usr/share/snmp/mibs:/usr/share/snmp/mibs/iana:/usr/share/snmp/mibs/ietf

##### 2. Editar archivo .conf

Aseguraos de editar vuestro archivo .conf con los datos relativos a vuestro InfluxDB y vuestro SAI.

##### 3. Importar el dashboard en Grafana

Tenéis también el JSON en este repositorio, el cual podéis utilizar al importar el dashboard en vuestro Grafana.
