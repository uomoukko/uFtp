WARNING:
uftp client uses an incoming port range only when in active mode
and it is compiled to use always this port-range
20500:21000 for ACTIVE FTP,  DATA:client<--server
you MUST open those ports in the client firewall.

if a ftpd server runs in the same machine
and it is configured to use a different port range let's say
20000:20500 for PASSIVE FTP,  DATA:client-->server,
then you MUST open those ports in the server firewall,too

If you want both ftp+ftpd, then the port range will be:
20000:20500(ftpd) + 20500:21000(ftp) = 20000:21000

NOW LET'S SEE HOW TO OPEN THOSE PORTS ON DGA4130 MODEM:
--------------------------------------------------------------------
firewall configuration for ftp-only: file /etc/config/firewall

config rule 'rule6i'
        option name 'open_port_20500:21000'
        option src 'wan'
        option proto 'tcp'
        option dest_port '20500:21000'
        option family 'ipv4'
        option target 'ACCEPT'
--------------------------------------------------------------------
firewall configuration for ftp+ftpd: file /etc/config/firewall

config rule 'rule6i'
        option name 'open_port_20000:21000'
        option src 'wan'
        option proto 'tcp'
        option dest_port '20000:21000'
        option family 'ipv4'
        option target 'ACCEPT'
--------------------------------------------------------------------
