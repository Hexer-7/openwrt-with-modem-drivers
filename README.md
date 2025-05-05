# Hi,

This is build of
openwrt 24.10.1 with quectel modem drivers QMI over usb or pcie for Banana Pi R4
Links on Release

For usb send these commands to the modem:
* AT+QCFG="usbnet",0
* AT+QCFG="data_interface",0,0

For pcie send these commands to the modem:
* AT+QCFG="usbnet",0
* AT+QCFG="data_interface",1,0
* AT+QCFG="pcie/mode",1

Make sure your sim is without PIN and there is PIN send:
AT+CPIN=Your SIM Pin



Then add new interface (or you can edit wan) and choose protocol "QMI Cellular" 
 and add your APN and if there is auth and choose IPv4 if your ISP not support IPv6
 and press "Save" and wait for seconds and it will work


## NOTE: to send AT commands install luci-app-atcommands ipk package in release,
it's for [4IceG](https://github.com/4IceG) btw.

