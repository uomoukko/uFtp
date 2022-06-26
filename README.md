# uFtp
![uftp.png](uftp.png)

## Very small micro ftp client
There are 4 architectures: Windows native, Windows/WSL, ARM-uClibc(old) ARM-linux(new)

## Getting started
Get the last release clicking on the **Releases** button
located on the **GitHUB** right panel<BR>
or just click [here](https://github.com/uomoukko/uFtp/releases/). It's free for *personal use*<BR>

# Prerequisites
    It will run on
    an ARM processor for the ARM version - two flavours: uClibc and glibc
    a x86 processor and WSL (needs Windows 10 Linux subsystem) for the WSL version
    a x86 processor and just Windows for the Windows version

## Running the executables
    example: uftp ftp.myserver.org
    or: uftp -a (anonymous mode)
    or: uftp ftp://john:secret@ftp.myserver.org:21/pub
    (syntax: uftp [-a] [proto://][[user][:pass]@]server[:port][/directories])

## Built with
**ARM-uclibc**: cross compiler ct-ng and gcc<BR>
**ARM-glibc** : cross compiler ct-ng and gcc<BR>
**x86-Win**: mingw-w64 gcc<BR>
**x86-WSL**: standard gcc<BR>

## Bugs
    Please contact me for bugs/improvements
    Keep in mind that this client HAS to be very skinny in order to fit in the router's ram.

