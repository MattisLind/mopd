# Booting a DECserver 100.

* Create the /tftpboot/mop folder
* Copy the PS0801ENG-New.SYS and PS0801ENG-Old.SYS to the /tftpboot/mop folder.
* Create a soft link from PS0801ENG.SYS to either the new or old file.
* Create a soft link from <MAC-address of DECserver>.SYS to the PS0801ENG.SYS. For example  08002b0413fe.SYS.

```
lrwxrwxrwx 1 root root     13 Jun 10 22:34 08002b0413fe.SYS -> PS0801ENG.SYS
-rw-rw-rw- 1 root root 110592 May  1  2001 PS0801ENG-New.SYS
-rw-rw-rw- 1 root root  65024 May  1  2001 PS0801ENG-Old.SYS
lrwxrwxrwx 1 root root     17 Jun 13 18:52 PS0801ENG.SYS -> PS0801ENG-New.SYS
```
* Set the interface in promiscous mode. ```/sbin/ifconfig eno0 promisc```
* Start mopd ```mopd -f eno0```


When the DECserver requests data it should look like this:

```
RSX Image
Header Block Count: 1
Image Size:         0001ad00
Load Address:       00000a76
Transfer Address:   00000a76
```

  * The DECserver 100 is connected to a standard male PC serial port (or USB dongle) with a straight cable DE9 - DB25. Pin 2 - Pin 2, Pin 3 - Pin 3 and Pin 5 - Pin 7.
