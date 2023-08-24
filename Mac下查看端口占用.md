1、查看端口号
```bash
# 可以使用netstat命令。netstat命令可以显示网络连接，路由表，接口状态，伪装连接，网络链路信息和组播成员组等信息。  
# 命令格式：netstat [选项]  
# 常用参数：

netstat [-AaLlnW] [-f address_family | -p protocol]  
netstat [-gilns] [-f address_family]  
netstat -i | -I interface [-w wait] [-abdgRt]  
netstat -s [-s] [-f address_family | -p protocol] [-w wait]  
netstat -i | -I interface -s [-f address_family | -p protocol]  
netstat -m [-m]  
netstat -r [-Aaln] [-f address_family]  
netstat -rs [-s]
```

```bash
#列出所有端口  
netstat   
  
#列出所有 tcp 端口   
netstat -at  
  
#显示网络接口列表  
netstat -i  
  
#显示网络工作信息统计表  
netstat -s  
  
#显示伪装的网络连线  
netstat -m  
  
#显示核心路由信息  
netstat -r  
  
#显示合并的信息  
netstat -rs  
routing:  
       	0 bad routing redirects  
       	0 dynamically created routes  
       	0 new gateways due to redirects  
       	4294944612 destinations found unreachable  
       	0 uses of a wildcard route  
       	8 routes not in table but not freed
```

2、查看某个端口占用
```bash
#命令格式：lsof -i :端口  
lsof -i:8080
```

```txt
# 控制台输出如下信息
COMMAND   PID   USER   FD   TYPE             DEVICE SIZE/OFF NODE NAME  
nginx     634 Jartto    6u  IPv4 0x8800c1295e443e43      0t0  TCP *:http-alt (LISTEN)  
nginx     635 Jartto    6u  IPv4 0x8800c1295e443e43      0t0  TCP *:http-alt (LISTEN)  
WeChat  93768 Jartto  119u  IPv6 0x8800c12977474f33      0t0  TCP 192.168.1.*
```

3、杀死进程
```bash
# 查看进程，命令行输入
ps -ef | more

# 找到需要杀掉的进程，执行
kill -9 pid

# 某种情况下，我们也可以根据进程名称来杀进程，如下
kill -9 name
```

