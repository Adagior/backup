# backup

线路查询

ipip.net

http://ping.pe

https://bgp.he.net/

https://ip.awk.sh

http://ip111.cn/

https://www.atrandys.com/2018/1214.html

备用命令


v2ray      https://233yes.com/post/1/

bbr
```
https://www.vultr.com/docs/how-to-deploy-google-bbr-on-centos-7


sudo rpm --import https://www.elrepo.org/RPM-GPG-KEY-elrepo.org
sudo rpm -Uvh http://www.elrepo.org/elrepo-release-7.0-2.el7.elrepo.noarch.rpm
sudo yum --enablerepo=elrepo-kernel install kernel-ml -y
sudo grub2-set-default 0
sudo shutdown -r now

echo 'net.core.default_qdisc=fq' | sudo tee -a /etc/sysctl.conf
echo 'net.ipv4.tcp_congestion_control=bbr' | sudo tee -a /etc/sysctl.conf
sudo sysctl -p

```
```
bash <(curl -s -L https://233yes.com/v2ray.sh)
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
firewall-cmd --zone=public --permanent --add-port=80/udp
firewall-cmd --zone=public --permanent --add-port=80/tcp
firewall-cmd --zone=public --permanent --add-port=8080/udp
firewall-cmd --zone=public --permanent --add-port=8080/tcp
firewall-cmd --zone=public --permanent --add-port=1200/udp
firewall-cmd --zone=public --permanent --add-port=27000-27050/udp
firewall-cmd --zone=public --permanent --add-port=27000-27050/tcp

firewall-cmd --zone=public --permanent --remove-service=ssh

systemctl restart firewalld.service

chmod a+x


sync; echo 3 > /proc/sys/vm/drop_caches
swapoff -a && swapon -a


screen -ls 
kill -9 pid
rm -rf /test

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
```
