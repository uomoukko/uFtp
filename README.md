# uFtp

This repository includes the executable files for my micro ftp client

[![DGA4130](img/DGA4130.png?raw=true)](exe/arm)
[![WINDOWS](img/win.png?raw=true)](exe/win)
[![WSL/WIN](img/wsl.png?raw=true)](exe/wsl)

## Getting started

Get the exe files for your architecture from the exe directory

# Prerequisites

You will need

a ARM uclibc processor for the ARM version

a x86 processor and WSL (windows linux subsystem) for the WSL version

a x86 processor and Windows for the Windows version

## Running the executables

    example: uftp ftp.myserver.org

    or: uftp -a

    or: uftp ftp.myserver.o:21

## Built with

*ARM-uclibc*: mini-native-arm4l.tar.bz2

*x86-Win*: mingw-w64

*x86-WSL*: standard gcc 7.3.0

## Bugs

Please tell me any bugs/improvements

but keep in mind that this client HAS to be very skinny

in order to fit in the router's ram.

