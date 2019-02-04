uftp may use a port range only when active mode
20500:21000 for ACTIVE FTP,  DATA:client<--server
you MUST open those ports in the client firewall.

if a ftpd is in the same machine and uses different port range let's say
20000:20500 for PASSIVE FTP,  DATA:client-->server,
then you MUST open those ports in the server firewall,too

If you want both ftp+ftpd, then the port range will be:
20000:20500(ftpd) + 20500:21000(ftp) = 20000:21000

firewall configuration for ftp only:

/etc/config/firewall

config rule 'rule6i'
        option name 'open_port_20500:21000'
        option src 'wan'
        option proto 'tcp'
        option dest_port '20000:21000'
        option family 'ipv4'
        option target 'ACCEPT'
