# Install
Tested on Ubuntu 16.04

```bash
sudo apt-get install -y \
build-essential libssl-dev libcurl4-openssl-dev libjansson-dev libgmp-dev automake zlib1g-dev && \
git clone https://github.com/MicroBitcoinOrg/Cpuminer.git cpuminer-opt-power2b && \
cd cpuminer-opt-power2b && \
./build-yespower.sh && \
./cpuminer --cputest
```

# Run
All address format (legacy, p2sh-segwit and ___bech32___) supported.

 * Mining Pool - `-t1` using 1 thread.
```
./cpuminer -a power2b -o stratum+tcp://micro-asia.skypool.co:8003 -u Was4hoWHCuxEUiE5gz8kdwj6T8DCFXdqJT -t1
```

 * Solo - `1650` is testnet. `-u` and `-p` is on the microd. `--no-longpoll` required to display netdiff correctly. 
```
./cpuminer -a power2b -o http://localhost:16501 --no-longpoll -u rpcuser -p 111111 --coinbase-addr=Was4hoWHCuxEUiE5gz8kdwj6T8DCFXdqJT -t1
```

 * Screenshot

![screenshot-cpuminer.png](https://i.imgur.com/TKWy4Zj.png)

-----

# README

This miner with `power2b` support is based on [cpuminer-opt-sugarchain](https://github.com/cryptozeny/cpuminer-opt-sugarchain) by **cryptozeny**.

cpuminer-opt is a fork of cpuminer-multi by TPruvot with optimizations
imported from other miners developped by lucas Jones, djm34, Wolf0, pooler,
Jeff garzik, ig0tik3d, elmad, palmd, and Optiminer, with additional
optimizations by Jay D Dee.

All of the code is believed to be open and free. If anyone has a
claim to any of it post your case in the cpuminer-opt Bitcoin Talk forum
or by email.

Miner programs are often flagged as malware by antivirus programs. This is
a false positive, they are flagged simply because they are cryptocurrency
miners. The source code is open for anyone to inspect. If you don't trust
the software, don't use it.

Requirements
------------

1. A x86_64 architecture CPU with a minimum of SSE2 support. This includes
Intel Core2 and newer and AMD equivalents. In order to take advantage of AES_NI
optimizations a CPU with AES_NI is required. This includes Intel Westbridge
and newer and AMD equivalents. Further optimizations are available on some
algoritms for CPUs with AVX and AVX2, Sandybridge and Haswell respectively.

Older CPUs are supported by cpuminer-multi by TPruvot but at reduced
performance.

ARM CPUs are not supported.

2. 64 bit Linux OS. Ubuntu and Fedora based distributions, including Mint and
Centos, are known to work and have all dependencies in their repositories.
Others may work but may require more effort. Older versions such as Centos 6
don't work due to missing features.
64 bit Windows OS is supported with mingw_w64 and msys or pre-built binaries.

MacOS, OSx and Android are not supported.

3. Stratum pool. Some algos may work wallet mining using getwork or GBT. YMMV.

Donations
---------

cpuminer-opt-power2b has no fees of any kind but donations are accepted.

 BTC: 31hMrody48EpQF4ZH3eFEd7CMJLPPCBHSe  
 ETH: 0x4c496e75bba93e084f54c56fd628539a8de7eba8  

Happy mining!
