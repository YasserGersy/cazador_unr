How to Detect SNMP services


Cazador Plugin : SNMP can be used to detect SNMP Services by sending  a request for the `system.sysDescr.0` value, which is present on almost all
SNMP enabled devices. This returned value gives us a description of the system software running on the device. 


Here is an example:

![ScreenShot](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/Snmp.Get.System.Desc.PNG?raw=true)


You can test dozens of hosts  by using CazadorSnmp, You can provide the hosts in one of the following formats:
- Domain names `xvulnerable.com`
- IPs  `192.168.1.102`
- Host:Port/IP addresses `192.168.1.102:161` `xvulnerable.com:161`
- HTTP urls also accepted `http://xvulnerable/`
- You can also define non standard ports 

The plugin allows you to  provide the targets via pasting or using a local file , The plugin will send a request for   `system.sysDescr` =  `1.3.6.1.2.1.1.1.0` ,
and it  will detect a running service if a response is received.



![ScreenShot](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/Snmp.Discovery.PNG?raw=true)



Inspired by : https://github.com/trailofbits/onesixtyone
