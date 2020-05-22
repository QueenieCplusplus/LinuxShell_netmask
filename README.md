# LinuxShell_netmask

* config  IP add

      ifconfig [interface_name] [param]
      
      ifconfig eth0 up // eth0 means one of the Network Interface. 網卡
      
      ifconfig eth0 192.168.0.2 netmask 255.255.255.0
    
* param
    
       +---------+----------------------------------+
       |  param  |               features           |                  
       +---------+----------------------------------+
       |    up   |         init this interface.     |
       +---------+----------------------------------+
       |  down   |       terminate this interface.  |
       +---------+----------------------------------+
       | netmask |                                  |
       +---------+----------------------------------+
       |broadcast|                                  |
       +---------+----------------------------------+
       | mtu + N |                                  |
       +---------+----------------------------------+
       |metric+ N|                                  |
       +---------+----------------------------------+
       
       and there are also the params including:
       
       arp
       promisc mode
       allmulti
    
