# uFtp
<TABLE><TR><TD>
<p align="center"><img src="img/uftp.png" alt="uftp-icon" width="250" height="250"></p>

<TABLE BORDER=0>
<TR>
<TD ALIGN=CENTER> <img src="img/win10.png"   alt="w10-icon"     width="100" height="100"><BR>Windows 10<BR></TD>
<TD ALIGN=CENTER> <img src="img/win11.png"   alt="w11-icon"     width="100" height="100"><BR>Windows 11<BR></TD>
<TD ALIGN=CENTER> <img src="img/wsl.png"     alt="wsl-icon"     width="100" height="100"><BR>Windows WSL<BR></TD>
<TD ALIGN=CENTER> <img src="img/DGA4130.png" alt="dga4130-icon" width="100" height="100"><BR>DGA4130<BR></TD>
<TD ALIGN=CENTER> <img src="img/DGA4331.png" alt="dga4331-icon" width="100" height="100"><BR>DGA4331<BR></TD>
</TR>
</TABLE>

# A very small micro ftp client
There are 3 architectures:<BR>
- Windows 64 bit signed PE32+ executable (console) x86-64<BR>
- Windows/WSL ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV) you need Linux subsystem<BR>
- armv7l-glibc(new) ELF 32-bit LSB executable, ARM, EABI5 version 1 (SYSV)<BR>
- ~~armv7l-uClibc not supported anymore because my modem firmware was upgraded to glibc, sorry~~<BR>

# Getting started
Get the last release clicking on the **Releases** button located on the **GitHUB** right panel<BR>
or just click [here](https://github.com/uomoukko/uFtp/releases/). It's free for *personal use*<BR>

# Running the executables
**example:**<BR>
C:\Users\Myname\Desktop> **uftp** ftp.myserver.org<BR>
C:\Users\Myname\Desktop> **uftp** -a *(anonymous mode)*<BR>
C:\Users\Myname\Desktop> **uftp** ftp://john:secret@ftp.myserver.org:21/pub<BR>
*(syntax: uftp [-a] [proto://][[user][:pass]@]server[:port][/directories])*<BR>

# Problems with WSL2
WSL1 can directly access the host's network interfaces and IP addresses without any additional configuration<BR>
WSL2 on the other way, when it starts, it is assigned a dynamic IP address from a private subnet (17.x.x.x)<BR>
because of this routing you will get this error:<BR>

`anonymous@ftp.external.com` A <- UFTP> dir<BR>
Client ready at 172.21.x.x:20500<BR>
PORT 172,21,x,x,80,20<BR>
500 I won't open a connection to 172.21.x.x (only to your.public.ip)

solution: give the command "mode passive", the prompt will change from A <- to P -><BR>
this means the client will always make outgoing connections to the server<BR>
be careful that the server must be on a public ip.<BR>

# Build notes
**x86-Windows**: built on Windows 10 using mingw-w64 gcc (10.3.0)<BR>

**x86-WSL**: built on Ubuntu WSL using standard gcc version 14.2.0 (Ubuntu 14.2.0-4ubuntu2)<BR>

**arm-glibc**: built on my DGA4331 modem (YES!)<BR>
toolchain was built by me on WSL linux (using crosstool-ng, canadian option).<BR>
the native arm gcc is version 14.1.0 (crosstool-NG 1.26.0.97_839bfbe)<BR>
then the toolchain was transferred to the modem's /opt/arm-unknown-linux-gnueabi (as a mounted usb disk)<BR>

# To do
Somedays I would like to implement FTPS/TLS using EXPLICIT MODE via "AUTH TLS"

# Bugs
Please contact me for bugs/improvements<BR>
*Keep in mind that this client HAS to be very skinny in order to fit in the router's ram.<BR>*
</TD></TR></TD></TABLE>
