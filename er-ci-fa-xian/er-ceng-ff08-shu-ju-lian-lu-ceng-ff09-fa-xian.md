## 二层发现（数据链路层）

### ARP协议扫描特点：

* ### 优点：

  扫描速度快，可靠性高。

* ### 缺点：

  不可路由，只能发现本网段内的主机。

## 扫描工具arping的使用：

* ### 基本语法：

* ### 常用命令:

  ```markdown
  #扫描某个IP主机是否存活
  root@kali:~# arping 192.168.5.1200 -c 1
  ARPING 192.168.5.175
  60 bytes from 00:0c:29:a8:30:72 (192.168.5.175): index=0 time=354.066 usec
  --- 192.168.5.175 statistics ---
  1 packets transmitted, 1 packets received, 0% unanswered (0 extra)
  rtt min/avg/max/std-dev = 0.354/0.354/0.354/0.000 ms

  #检测网段内是否有arp欺骗
  arping 192.168.1.1 -d
  
  #过滤出存活主机IP地址：
  root@kali:~# arping 192.168.5.175 -c 1|grep "bytes from"|cut -d" " -f 5|cut -d"(" -f 2|cut -   d")" -f 1
192.168.5.175
  ```
* ### 脚本编写：

  > ##### 1.扫描网段内所有存活的主机：

  ```markdown
  #!/bin/bash
  ```

  > ##### 2.扫描网段内自定义的IP地址：

  ```markdown
  dfgdfsg
  ```



