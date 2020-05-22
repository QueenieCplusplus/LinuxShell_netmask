# LinuxShell_netmask

* config  IP add

      ifconfig [interface_name] [param] // if means interface
      
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
    
* example

      ✗ ifconfig
      
      lo0: flags=8049<UP,LOOPBACK,RUNNING,MULTICAST> 
            mtu 16384
            options=1203<RXCSUM,TXCSUM,TXSTATUS,SW_TIMESTAMP>
            inet 127.0.0.1 // 網路位址
            netmask 0xff000000 //子網路遮罩
            
            inet6 ::1 
            prefixlen 128 
            inet6 fe80::1
            %lo0 
            prefixlen 64 
            scopeid 0x1 
            nd6 options=201<PERFORMNUD,DAD>
            
      gif0: flags=8010
            <POINTOPOINT,MULTICAST> 
            mtu 1280

      en0: flags=8863
            <UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> 
            mtu 1500
            options=400<CHANNEL_IO>
            ether 60:03:08:96:dd:bb //網卡卡號
            inet6 fe80::18a1:1e87:7a99:966c
            %en0 
            prefixlen 64 
            secured scopeid 0x4 
            inet 192.168.100.24 //網路位址
            netmask 0xffffff00 //子網路遮罩
            broadcast 192.168.100.255 //廣播
            
            nd6 options=201<PERFORMNUD,DAD>
            media: autoselect
            status: active
            
      awdl0: flags=8943
            <UP,BROADCAST,RUNNING,PROMISC,SIMPLEX,MULTICAST> 
            mtu 1484
            options=400<CHANNEL_IO>
            ether 0e:56:6b:69:99:66
            inet6 fe80::c56:6bff:fe69:9660% 
            awdl0 
            prefixlen 64 
            scopeid 0x9 
            nd6 options=201<PERFORMNUD,DAD>
            media: autoselect
            status: active
            
      llw0: flags=8863
             <UP,BROADCAST,SMART,RUNNING,SIMPLEX,MULTICAST> 
            mtu 1500
            options=400<CHANNEL_IO>
            ether 0e:56:6b:69:99:66 
            inet6 fe80::c56:6bff:fe69:9666
            %llw0 prefixlen 64 scopeid 0xa 
            nd6 options=201<PERFORMNUD,DAD>
            media: autoselect
            status: active
            
      utun0: flags=8051
            <UP,POINTOPOINT,RUNNING,MULTICAST> 
            mtu 1380
            inet6 fe80::6a93:5630:89ed:3e55
            %utun0 prefixlen 64 scopeid 0xb 
            nd6 options=201<PERFORMNUD,DAD>
