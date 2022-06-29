# uFtp
![uftp.png](uftp.png)

## Very small micro ftp client
There are 4 architectures:<BR>
- Windows native<BR>
- Windows/WSL<BR>
- armv7l-uClibc(old)<BR>
- armv7l-glibc(new)<BR>

## Getting started
Get the last release clicking on the **Releases** button located on the **GitHUB** right panel<BR>
or just click [here](https://github.com/uomoukko/uFtp/releases/). It's free for *personal use*<BR>

# Prerequisites
It will run on<BR>
- armv7l in two flavours: uClibc and glibc<BR>
- x86 and WSL *(needs Windows 10 Linux subsystem)*<BR>
- x86 and just Windows<BR>

## Running the executables
**example:**<BR>
C:\Users\Myname\Desktop>**uftp** ftp.myserver.org<BR>
C:\Users\Myname\Desktop>**uftp** -a *(anonymous mode)*<BR>
C:\Users\Myname\Desktop>**uftp** ftp://john:secret@ftp.myserver.org:21/pub<BR>
*(syntax: uftp [-a] [proto://][[user][:pass]@]server[:port][/directories])*<BR>

## Built with
**arm-glibc/uClibc**: built on WSL using gcc (11.2.0) to build a cross compiler<BR>
**x86-Windows**: built on Windows using mingw-w64 gcc (10.3.0)<BR>
**x86-WSL**: built on WSL using gcc (11.2.0)<BR>

## Bugs
Please contact me for bugs/improvements<BR>
*Keep in mind that this client HAS to be very skinny in order to fit in the router's ram.<BR>*

