# uFtp

<img src="img/uftp-242.png" alt="Exeicon" width="200" height="200"><BR>
<TABLE>
  <TR>
    <TD> <img src="img/win10.png" alt="w10icon" width="100" height="100"><BR>
      For Windows 10<BR>
    </TD>
    <TD> <img src="img/win11.png" alt="w11icon" width="100" height="100"><BR>
      For Windows 11<BR>
    </TD>
     <TD> <img src="img/wsl.png" alt="wslicon" width="100" height="100"><BR>
      For Windows WSL<BR>
    </TD>
  </TR>
</TABLE>
<TABLE>
 <TR>
  <TD> <img src="img/DGA4130.png" alt="dga4130icon" width="100" height="100"><BR>
      For DGA4130<BR>
  </TD>
   <TD> <img src="img/DGA4331.png" alt="dga4331icon" width="100" height="100"><BR>
      For DGA4331<BR>
    </TD>
  </TR>
</TABLE>

## Very small micro ftp client
There are 3 architectures:<BR>
- Windows native<BR>
- Windows/WSL<BR>
- armv7l-glibc(new)<BR>
no more armv7l-uClibc, sorry<BR>

## Getting started
Get the last release clicking on the **Releases** button located on the **GitHUB** right panel<BR>
or just click [here](https://github.com/uomoukko/uFtp/releases/). It's free for *personal use*<BR>

# Prerequisites
It will run on<BR>
- armv7l with glibc<BR>
- x86 and WSL *(needs Windows 10/11 Linux subsystem)*<BR>
- x86 and just Windows<BR>

## Running the executables
**example:**<BR>
C:\Users\Myname\Desktop>**uftp** ftp.myserver.org<BR>
C:\Users\Myname\Desktop>**uftp** -a *(anonymous mode)*<BR>
C:\Users\Myname\Desktop>**uftp** ftp://john:secret@ftp.myserver.org:21/pub<BR>
*(syntax: uftp [-a] [proto://][[user][:pass]@]server[:port][/directories])*<BR>

## Built with (updated)
**x86-Windows**: built on Windows using mingw-w64 gcc (10.3.0)<BR>

**x86-WSL**: built on ubuntu WSL using standard gcc version 14.2.0 (Ubuntu 14.2.0-4ubuntu2)<BR>

**arm-glibc**: built on DGA4331 modem. Compiler in /opt/arm-unknown-linux-gnueabi<BR>
gcc is version 14.1.0 (crosstool-NG 1.26.0.97_839bfbe)<BR>
compiler was built on WSL linux (crosstool-ng, canadian option) by me and transferred to the modem's external usb disk<BR>



## To do
Implement FTPS/TLS using EXPLICIT MODE via "AUTH TLS"

## Bugs
Please contact me for bugs/improvements<BR>
*Keep in mind that this client HAS to be very skinny in order to fit in the router's ram.<BR>*

