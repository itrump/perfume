# 日常

## Coding
- ssh如何通过代理连接远程主机？
  - 在local机器上要连接主机A，但local机器ping不通主机A，
       也ssh连不上主机A，可通过local机器上运行socks5代理，
       并配置 ~/.ssh/config来解决
    - mac 上的配置如下
    - ```Host *.*.*.* # 匹配任一ip或含4个字段的域名 ```
    - ```    ProxyCommand nc -X 5 -x local_host_ip:local_port %h %p # 将local_host_ip local_port替换为真正的代理地址```
    - 上面5代表使用sock5代理
  - 当然如果代理运行在远程，则将local_host_ip:local_port替换为远程ip和端口即可。

