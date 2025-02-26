# sudo-command
Practice creating new users and groups and viewing groups
┌──(kali㉿kali)-[~]
└─$ cd ..      
                                                                                        
┌──(kali㉿kali)-[/home]
└─$ ll      
total 4
drwx------ 32 kali kali 4096 Feb 26 09:02 kali
                                                                                        
┌──(kali㉿kali)-[/home]
└─$ sudo adduser ojie                               
[sudo] password for kali: 
info: Adding user `ojie' ...
info: Selecting UID/GID from range 1000 to 59999 ...
info: Adding new group `ojie' (1001) ...
info: Adding new user `ojie' (1001) with group `ojie (1001)' ...
info: Creating home directory `/home/ojie' ...
info: Copying files from `/etc/skel' ...
New password: 
Retype new password: 
passwd: password updated successfully
Changing the user information for ojie
Enter the new value, or press ENTER for the default
        Full Name []: ojie
        Room Number []: 112
        Work Phone []: 0250255025       
        Home Phone []: 0245892475
        Other []: nil 
Is the information correct? [Y/n] y
info: Adding new user `ojie' to supplemental / extra groups `users' ...
info: Adding user `ojie' to group `users' ...
                                                                                        
┌──(kali㉿kali)-[/home]
└─$ sudo groupadd important
                                                                                        
┌──(kali㉿kali)-[/home]
└─$ sudo usermod -aG important ojie
                                                                                        
┌──(kali㉿kali)-[/home]
└─$ ll
total 8
drwx------ 32 kali kali 4096 Feb 26 09:02 kali
drwx------  5 ojie ojie 4096 Feb 26 09:04 ojie
                                                                                        
┌──(kali㉿kali)-[/home]
└─$ sudo cat /etc/passwd           
root:x:0:0:root:/root:/usr/bin/zsh
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/run/ircd:/usr/sbin/nologin
_apt:x:42:65534::/nonexistent:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
systemd-network:x:998:998:systemd Network Management:/:/usr/sbin/nologin
systemd-timesync:x:997:997:systemd Time Synchronization:/:/usr/sbin/nologin
messagebus:x:100:107::/nonexistent:/usr/sbin/nologin
tss:x:101:109:TPM software stack,,,:/var/lib/tpm:/bin/false
strongswan:x:102:65534::/var/lib/strongswan:/usr/sbin/nologin
tcpdump:x:103:110::/nonexistent:/usr/sbin/nologin
usbmux:x:104:46:usbmux daemon,,,:/var/lib/usbmux:/usr/sbin/nologin
sshd:x:105:65534::/run/sshd:/usr/sbin/nologin
dnsmasq:x:106:65534:dnsmasq,,,:/var/lib/misc:/usr/sbin/nologin
avahi:x:107:112:Avahi mDNS daemon,,,:/run/avahi-daemon:/usr/sbin/nologin
speech-dispatcher:x:108:29:Speech Dispatcher,,,:/run/speech-dispatcher:/bin/false
pulse:x:109:114:PulseAudio daemon,,,:/run/pulse:/usr/sbin/nologin
lightdm:x:110:116:Light Display Manager:/var/lib/lightdm:/bin/false
saned:x:111:118::/var/lib/saned:/usr/sbin/nologin
polkitd:x:996:996:polkit:/nonexistent:/usr/sbin/nologin
rtkit:x:112:119:RealtimeKit,,,:/proc:/usr/sbin/nologin
colord:x:113:120:colord colour management daemon,,,:/var/lib/colord:/usr/sbin/nologin
nm-openvpn:x:114:121:NetworkManager OpenVPN,,,:/var/lib/openvpn/chroot:/usr/sbin/nologin
nm-openconnect:x:115:122:NetworkManager OpenConnect plugin,,,:/var/lib/NetworkManager:/usr/sbin/nologin
mysql:x:116:124:MySQL Server,,,:/nonexistent:/bin/false
stunnel4:x:995:995:stunnel service system account:/var/run/stunnel4:/usr/sbin/nologin
_rpc:x:117:65534::/run/rpcbind:/usr/sbin/nologin
geoclue:x:118:126::/var/lib/geoclue:/usr/sbin/nologin
Debian-snmp:x:119:127::/var/lib/snmp:/bin/false
sslh:x:120:128::/nonexistent:/usr/sbin/nologin
ntpsec:x:121:131::/nonexistent:/usr/sbin/nologin
redsocks:x:122:132::/var/run/redsocks:/usr/sbin/nologin
rwhod:x:123:65534::/var/spool/rwho:/usr/sbin/nologin
_gophish:x:124:134::/var/lib/gophish:/usr/sbin/nologin
iodine:x:125:65534::/run/iodine:/usr/sbin/nologin
miredo:x:126:65534::/var/run/miredo:/usr/sbin/nologin
statd:x:127:65534::/var/lib/nfs:/usr/sbin/nologin
redis:x:128:135::/var/lib/redis:/usr/sbin/nologin
postgres:x:129:136:PostgreSQL administrator,,,:/var/lib/postgresql:/bin/bash
mosquitto:x:130:138::/var/lib/mosquitto:/usr/sbin/nologin
inetsim:x:131:139::/var/lib/inetsim:/usr/sbin/nologin
_gvm:x:132:141::/var/lib/openvas:/usr/sbin/nologin
kali:x:1000:1000:,,,:/home/kali:/usr/bin/zsh
_galera:x:133:65534::/nonexistent:/usr/sbin/nologin
Debian-exim:x:134:144::/var/spool/exim4:/usr/sbin/nologin
cups-pk-helper:x:135:145:user for cups-pk-helper service,,,:/nonexistent:/usr/sbin/nologin
rayel:x:1002:1002:Racheal Esangbedo,12,07780637259,07780637259,nil:/home/rayel:/bin/bash
ojie:x:1001:1001:ojie,112,0250255025,0245892475,nil:/home/ojie:/bin/bash
                                                                                        
┌──(kali㉿kali)-[/home]
└─$ sudo groups ojie       
ojie : ojie users important
                                                                                        
┌──(kali㉿kali)-[/home]
└─$ sudo cat /etc/group 
root:x:0:
daemon:x:1:
bin:x:2:
sys:x:3:
adm:x:4:kali
tty:x:5:
disk:x:6:
lp:x:7:
mail:x:8:
news:x:9:
uucp:x:10:
man:x:12:
proxy:x:13:
kmem:x:15:
dialout:x:20:kali
fax:x:21:
voice:x:22:
cdrom:x:24:kali
floppy:x:25:kali
tape:x:26:
sudo:x:27:kali
audio:x:29:pulse,kali
dip:x:30:kali
www-data:x:33:
backup:x:34:
operator:x:37:
list:x:38:
irc:x:39:
src:x:40:
shadow:x:42:
utmp:x:43:
video:x:44:kali
sasl:x:45:
plugdev:x:46:kali
staff:x:50:
games:x:60:
users:x:100:kali,rayel,ojie
nogroup:x:65534:
systemd-journal:x:999:
systemd-network:x:998:
crontab:x:101:
input:x:102:
sgx:x:103:
kvm:x:104:
render:x:105:
netdev:x:106:kali
systemd-timesync:x:997:
messagebus:x:107:
_ssh:x:108:
tss:x:109:
tcpdump:x:110:
bluetooth:x:111:kali
avahi:x:112:
pipewire:x:113:
pulse:x:114:
pulse-access:x:115:
lightdm:x:116:
scanner:x:117:saned,kali
saned:x:118:
polkitd:x:996:
rtkit:x:119:
colord:x:120:
nm-openvpn:x:121:
nm-openconnect:x:122:
kali-trusted:x:123:
mysql:x:124:
rdma:x:125:
stunnel4:x:995:stunnel4
geoclue:x:126:
Debian-snmp:x:127:
sslh:x:128:
ssl-cert:x:129:postgres
i2c:x:130:
ntpsec:x:131:
redsocks:x:132:
kismet:x:133:
_gophish:x:134:
redis:x:135:_gvm
postgres:x:136:
plocate:x:137:
mosquitto:x:138:
sambashare:x:994:
inetsim:x:139:
wireshark:x:140:kali
_gvm:x:141:
kali:x:1000:
kaboxer:x:142:kali
vboxsf:x:143:kali
Debian-exim:x:144:
lpadmin:x:145:
winbindd_priv:x:993:
rayel:x:1002:
hackers:x:1003:
ojie:x:1001:
important:x:1004:ojie
