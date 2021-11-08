---
layout: page
title: Quick Start - Linux
nav_exclude: true
permalink: /docs/quickstart/linux
---

# Quick Start - Linux
{: .no_toc }

This guide will help you install and build your first PcapPlusPlus application on Linux in a few simple steps.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Step 1 - install PcapPlusPlus

Before installing PcapPlusPlus make sure you have the prerequisites installed for [Linux]({{ site.baseurl }}/docs/install/build-source/linux#prerequisites).

Pre-compiled packages are available for recent versions of Ubuntu, Fedora and CentOS. You can find them under the [{{ site.pcapplusplus_ver }} release page](https://github.com/seladb/PcapPlusPlus/releases/tag/{{site.pcapplusplus_ver}}). After downloading and extracting the archive file go to: `/path/to/your/package/` and run the installation script:

```shell
./install.sh
```

Another option is using [Homebrew on Linux](https://docs.brew.sh/Homebrew-on-Linux) if you have it installed on your system:

```shell
brew install pcapplusplus
```

If you have other Linux distribution, another version of the distribution mentioned above or other GCC version you'll need to [build PcapPlusPlus from source]({{ site.baseurl }}/docs/install/build-source/linux). Make sure not to skip the [installation]({{ site.baseurl }}/docs/install/build-source/linux#installation) part.

## Step 2 - create your first app

If you downloaded a pre-compiled package go to: `/path/to/your/package/example-app`.

If you built it from source go to: `/path/to/pcapplusplus/source/Tutorials/Tutorial-HelloWorld`.

Make sure you see the following files:

```shell
 |-- main.cpp
 |-- 1_packet.pcap
```

`main.cpp` is the example application we'll use.

`1_packet.pcap` is a pcap file the app reads from.

## Step 3 - create a Makefile

If you downloaded a pre-compiled package you can find a Makefile in `/path/to/your/package/example-app`. This Makefile is already configured.

If you built it from source:

- go to `/path/to/pcapplusplus/source/Tutorials/Tutorial-HelloWorld`
- rename `Makefile.non_windows` to `Makefile`

## Step 4 - build and run your app

Run `make` to build the app:

```shell
$ make
```

An executable file will be created which contains the compiled app. You can now run it and should be able to see the following output:

```shell
Source IP is '10.0.0.138'; Dest IP is '10.0.0.1'
```
