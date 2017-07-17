### stop default services

systemctl disable postfix

systemctl disable remote-fs.target

systemctl disable tuned.service

systemctl disable kdump

systemctl disable irqbalance

systemctl disable NetworkManager

### init firewalld

yum install -y firewalld

firewall-cmd --remove-service dhcpv6-client

firewall-cmd --remove-service dhcpv6-client --permanent
