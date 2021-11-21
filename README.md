# backup

gfwlist

https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt

dns

https://www.publicdns.xyz/

https://ilpl.me/2018/08/17/public-DNS-5353-list/

线路查询

ipip.net

http://ping.pe

https://bgp.he.net/

https://ip.awk.sh

http://ip111.cn/

https://www.atrandys.com/2018/1214.html


软件源

https://www.moerats.com/archives/784/






备用命令

测试
```
wget -qO- bench.sh | bash
wget -N --no-check-certificate https://raw.githubusercontent.com/chiakge/Linux-Server-Bench-Test/master/linuxtest.sh
bash linuxtest.sh a

https://www.moerats.com/archives/626/
```
bbr
```
https://www.vultr.com/docs/how-to-deploy-google-bbr-on-centos-7


sudo rpm --import https://www.elrepo.org/RPM-GPG-KEY-elrepo.org
sudo rpm -Uvh http://www.elrepo.org/elrepo-release-7.0-3.el7.elrepo.noarch.rpm
sudo yum --enablerepo=elrepo-kernel install kernel-ml -y
sudo grub2-set-default 0
sudo shutdown -r now

echo 'net.core.default_qdisc=fq' | sudo tee -a /etc/sysctl.conf
echo 'net.ipv4.tcp_congestion_control=bbr' | sudo tee -a /etc/sysctl.conf
sudo sysctl -p

```

socat
```
bash <(curl -s -L https://233yes.com/v2ray.sh)

yum install -y socat
socat TCP4-LISTEN:10000,reuseaddr,fork TCP4:1.1.1.1:10000 >> socat.log 2>&1 &
socat UDP4-LISTEN:10000,reuseaddr,fork UDP4:1.1.1.1:10000 >> socat.log 2>&1 &
```
trojan
```
tar -Jxf 
nohup trojan >/dev/null 2>&1 &
```

bbr
```
wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh
```


shadowsocksr
```
  wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh
  chmod +x shadowsocksR.sh
  ./shadowsocksR.sh 2>&1 | tee shadowsocksR.log
```

fail2ban
```
wget --no-check-certificate https://raw.githubusercontent.com/FunctionClub/Fail2ban/master/fail2ban.sh && bash fail2ban.sh 2>&1 | tee fail2ban.log
```

```
firewall-cmd --zone=public --permanent --add-port=53/udp
firewall-cmd --zone=public --permanent --add-port=53/tcp
firewall-cmd --zone=public --permanent --add-port=80/udp
firewall-cmd --zone=public --permanent --add-port=80/tcp
firewall-cmd --zone=public --permanent --add-port=8080/udp
firewall-cmd --zone=public --permanent --add-port=8080-8088/tcp
firewall-cmd --zone=public --permanent --add-port=443/udp
firewall-cmd --zone=public --permanent --add-port=443/tcp
firewall-cmd --zone=public --permanent --add-port=1200/udp
firewall-cmd --zone=public --permanent --add-port=27000-27050/udp
firewall-cmd --zone=public --permanent --add-port=27000-27050/tcp
firewall-cmd --zone=public --permanent --add-port=3478-3479/udp
firewall-cmd --zone=public --permanent --add-port=5060-5062/udp
firewall-cmd --zone=public --permanent --add-port=12000-29999/udp
firewall-cmd --zone=public --permanent --add-port=32801-32825/udp
firewall-cmd --zone=public --permanent --add-port=3128/tcp
firewall-cmd --zone=public --permanent --add-port=3659/tcp
firewall-cmd --zone=public --permanent --add-port=8888/tcp
firewall-cmd --zone=public --permanent --add-port=20000-26000/tcp
firewall-cmd --zone=public --permanent --add-port=32801-32803/tcp
firewall-cmd --zone=public --permanent --add-port=10011-10019/tcp
firewall-cmd --zone=public --permanent --add-port=5063/udp

firewall-cmd --zone=public --permanent --add-port=8877/tcp
firewall-cmd --zone=public --permanent --add-port=8877/udp
firewall-cmd --zone=public --permanent --add-port=8899/tcp
firewall-cmd --zone=public --permanent --add-port=8899/udp
firewall-cmd --zone=public --permanent --add-port=11111/tcp
firewall-cmd --zone=public --permanent --add-port=11111/udp
firewall-cmd --zone=public --permanent --add-port=1990/tcp
firewall-cmd --zone=public --permanent --add-port=1990/udp

firewall-cmd --add-masquerade --permanent
firewall-cmd --permanent --add-forward-port=port=8888:proto=tcp:toaddr=?.?.?.?:toport=8877
firewall-cmd --permanent --add-forward-port=port=8888:proto=udp:toaddr=?.?.?.?:toport=8877

firewall-cmd --zone=public --permanent --remove-service=ssh

systemctl restart firewalld.service

firewall-cmd --direct --remove-rule ipv4 nat POSTROUTING 0 -s 10.8.0.0/24 ! -d 10.8.0.0/24 -j SNAT --to ?.?.?.?
firewall-cmd --permanent --direct --remove-rule ipv4 nat POSTROUTING 0 -s 10.8.0.0/24 ! -d 10.8.0.0/24 -j SNAT --to ?.?.?.?
firewall-cmd --direct --add-rule ipv4 nat POSTROUTING 0 -s 10.8.0.0/24 ! -d 10.8.0.0/24 -j SNAT --to ?.?.?.?
firewall-cmd --permanent --direct --add-rule ipv4 nat POSTROUTING 0 -s 10.8.0.0/24 ! -d 10.8.0.0/24 -j SNAT --to ?.?.?.?

netstat -na|grep ESTABLISHED|awk '{print $5}'|awk -F: '{print $1}'
 
chmod a+x

sync; echo 3 > /proc/sys/vm/drop_caches
swapoff -a && swapon -a


screen -ls 
kill -9 pid
rm -rf /test
echo 3 > /proc/sys/vm/drop_caches && swapoff -a && swapon -a && printf '\n%s\n' 'Ram-cache and Swap Cleared'

vi /etc/crontab
30 19 * * * root reboot
* */1 * * * root sync; echo 3 > /proc/sys/vm/drop_caches
* */1 * * * root swapoff -a && swapon -a
systemctl enable crond.service
systemctl start crond

vi /etc/ssh/sshd_config  

/etc/rc.d/rc.local
nohup ？？？ >/dev/null 2>&1 &

yum install mtr -y
yum install net-tools -y
yum install bind-utils -y


```

openssl

https://blog.csdn.net/oLiuKong/article/details/52077754

asf

https://steamcn.com/t413908-1-1


socat 

https://www.moerats.com/archives/97/

v2ray  

https://233yes.com/post/1/

https://raw.githubusercontent.com/233boy/v2ray/master/install.sh

https://github.com/KiriKira/vTemplate
