# uFtp

This repository includes the executable files for my micro ftp client

## Getting started

Get the exe files for your architecture pushing the "RELEASE" button

# Prerequisites

You will need

a ARM processor for the ARM version

a x86 processor and WSL (windows linux subsystem) for the WSL version

a x86 processor and Windows for the Windows version

## Running the executables

    example: uftp ftp.myserver.org

    or: uftp -a

    or: uftp ftp.myserver.o:21

## Built with

*ARM-uclibc*: cross compiler ct-ng
*ARM-linux*: cross compiler ct-ng

*x86-Win*: mingw-w64

*x86-WSL*: standard gcc 7.3.0

## Bugs

Please tell me any bugs/improvements

but keep in mind that this client HAS to be very skinny

in order to fit in the router's ram.

