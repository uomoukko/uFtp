# uFtp

This repository includes the *executable files* for my micro ftp client

## Getting started

Get the exe files for your architecture pushing the "RELEASE" button

There are 4 architectures: Windows native, Windows/WSL, ARM-uClibc(old) ARM-linux(new)

# Prerequisites

It wil run on

an ARM processor for the ARM version

a x86 processor and WSL (windows linux subsystem) for the WSL version

a x86 processor and Windows for the Windows version

## Running the executables

    example: uftp ftp.myserver.org

    or: uftp -a (anonymous mode)

    or: uftp ftp://john:secret@ftp.myserver.org:21/pub

    (syntax: uftp [-a] [proto://][[user][:pass]@]server[:port][/directories])

## Built with

*ARM-uclibc*: cross compiler ct-ng

*ARM-linux* : cross compiler ct-ng

*x86-Win*: mingw-w64

*x86-WSL*: standard gcc 10.2.0

## Bugs

Please write me any bugs/improvements

but keep in mind that this client HAS to be very skinny

in order to fit in the router's ram.

