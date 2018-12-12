# openvpn one-click install 
## Summary
Openvpn one-click install is a shell to delpoy Openvpn server with User/Pass & certificate authentication on Linux system.



## Prerequisite
* GNU/Linux with Bash and root access
* wget


### CentOS 7
1. Download the file from release
```
# cd ~
# yum install -y git
# git clone https://github.com/razerkin/one-click-openvpn ~/openvpn
```
2. Edit the database information
```
# vi openvpn/openvpn.sh
# HOSTNAME="localhost"
# PORT="3306"
# USERNAME="root"
# PASSWORD=""
# DBUSER="vpnadmin"
# DBPWD="vpnadminpwd"
# USERCERTNAME="vpnuser"
```
3. Run the shell to install openvpn,mysql,iptables...
```
# source ~/openvpn/openvpn.sh
```
4. Edit the client.conf and donwload it to connect your server.
```
# sz ~/openvpn/client.conf
```
then copy and replace the ca.crt,ta.key,user's key&cert in the file.

5.connect, complete.


## Usage
* Start On Server
* Add/Delete User (use mysql);
* User Run OPENVPN

## Use of
* OpenVPN
* Mysql
* iptables
* ...
