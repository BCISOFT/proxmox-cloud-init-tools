# Proxmox cloud-init tools
ShellScript tools to deploy VM cloud-init in Proxmox Virtual Environment (PVE)

### Supported PVE Versions
- PVE 6 *Not tested*
- PVE 6.1 **[OK] - Tested**
- PVE 6.2 **[OK] - Tested**
- PVE 6.3 **[OK] - Tested**
- PVE 7.4 **[OK] - Tested**

### Features
1. Auto cloud images download
- Debian 9 - Stretch
- Debian 10 - Buster
- Debian 11 - Bullseye
- Debian 12 - Bookworm
- Ubuntu Server 18.04 LTS - Bionic
- Ubuntu Server 20.04 LTS - Focal
- Ubuntu Server 22.04 LTS - Jammy
- OpenSUSE LEAP 15.2
- Centos 8
2. Set VM Hostname
3. Set VM Description
4. Memory (Available to select 2GB,4GB,8GB and 16GB)
5. CPU Cores
6. CPU Sockets
7. Storage destination (Local, NFS, LVM/LVM-Thin, etc)
8. Storage disk size
9. Define user, by default root user is defined. If you change to another, this user can be used with sudo powers without password;
10. Insert SSH authorized keys to user defined on step 8 **Very important**;
11. Select bridge network;
12. Select Static/IP or DHCP usage;
13. Define uniq VMID;
14. Can start or not, VM after deployment.

### Usage
1. Login on your Proxmox VE server over SSH or Console Shell
2. Clone proxmox-cloud-init project
```
git clone https://github.com/kmee/proxmox-cloud-init-tools.git
```
```
cd proxmox-cloud-init-tools
```
3. Create authorized keys files
```
mkdir pub_keys
```
```
touch pub_keys/id_rsa.pub
```
**copy your public ssh keys to pub/keys/id_rsa.pub file**

4. Adjust permission, then run deploy.sh
```
chmod +x deploy.sh
```
```
./deploy.sh
```
5. Follow instructions on screen.

### Important
Before deploy VM using things script, upload your public ssh key to ./pub_keys/id_rsa.pub file.
if you do not upload keys do pub_keys/id_rsa.pub, you will not access VM.

### Contributors
Ananias Filho - @ananiasfilho

Frederico Siena 
