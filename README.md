# SNMP Simulator

This docker image starts up snmpsim.

The UDP port `161` should be mapped to the desired SNMP port.

This image does not contain any snmpwalks. You should mount a folder with snmpwalks like this:

    docker run -v /somewhere/with/snmpwalks:/usr/share/snmpsim/data \
               -p 161:161/udp \
               tandrup/private-bower

