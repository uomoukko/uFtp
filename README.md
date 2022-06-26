# uFtp
![uftp.png](uftp.png)

## Very small micro ftp client
There are 4 architectures:<BR>
Windows native<BR>
Windows/WSL<BR>
armv7l-uClibc(old)<BR>
armv7l-glibc(new)<BR>

## Getting started
Get the last release clicking on the **Releases** button located on the **GitHUB** right panel<BR>
or just click [here](https://github.com/uomoukko/uFtp/releases/). It's free for *personal use*<BR>

# Prerequisites
It will run on<BR>
an ARM processor for the ARM version - two flavours: uClibc and glibc<BR>
a x86 processor and WSL (needs Windows 10 Linux subsystem) for the WSL version<BR>
a x86 processor and just Windows for the Windows version<BR>

## Running the executables
example: uftp ftp.myserver.org<BR>
or: uftp -a (anonymous mode)<BR>
or: uftp ftp://john:secret@ftp.myserver.org:21/pub<BR>
\(syntax: uftp [-a] [proto://][[user][:pass]@]server[:port][/directories])<BR>

## Built with
**ARM-uclibc**: cross compiler ct-ng and gcc<BR>
**ARM-glibc** : cross compiler ct-ng and gcc<BR>
**x86-Win**: mingw-w64 gcc<BR>
**x86-WSL**: standard gcc<BR>

## Bugs
Please contact me for bugs/improvements<BR>
*Keep in mind that this client HAS to be very skinny in order to fit in the router's ram.<BR>*

