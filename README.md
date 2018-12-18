# <span style="color:#E91E63">C</span>rypto<span style="color:#03A9F4">D</span>redge

## Overview

CryptoDredge is a simple in use and highly optimized cryptocurrency mining software. It takes full advantage of modern <span style="color:#76b900">NVIDIA</span> graphics cards through the use of unique optimization techniques. We have also devoted great attention to stable power consumption. These benefits, along with the very small developer fee, make our product one of the best publicly available miners.

## Features

Developer fee is 1%

## Supported Algorithms

- Allium
- BCD
- BitCore
- Blake (2s)
- C11
- CryptoLightV7    (Aeon)
- CryptoNightFast  (Masari)
- CryptoNightHaven
- CryptoNightHeavy
- CryptoNightSaber (Bittube)
- CryptoNightV7
- CryptoNightV8    (Monero)
- Dedal
- Exosis
- HMQ1725
- Lbk3
- Lyra2REv2
- Lyra2REv3
- Lyra2vc0ban
- Lyra2z
- NeoScrypt
- PHI1612
- Phi2
- Pipe
- Polytimos
- Skein
- Skunkhash
- Stellite
- Tribus
- X16R
- X16S
- X17 
- X21S
- X22i

## QuickStart

The current version of CryptoDredge is a (portable) console application. Unpack the downloaded archive and edit one of the sample `.bat`/`.sh` files or provide the necessary command line arguments.

Example:

```
CryptoDredge -a <ALGO> -o stratum+tcp://<POOL> -u <WALLET_ADDRESS> -p <OPTIONS>
```

## Command-Line Arguments

`-v`, `--version` Print version information

`-a`, `--algo` Specify algorithm to use
- `aeon` (CryptoNight-Lite algorithm)
- `allium`
- `bcd`
- `bitcore`
- `blake2s`
- `c11`
- `cnfast` (Masari)
- `cnhaven`
- `cnheavy`
- `cnsaber` (BitTube)
- `cnv7`
- `cnv8` (Monero)
- `dedal`
- `exosis`
- `hmq1725`
- `lbk3`
- `lyra2v2`
- `lyra2v3`
- `lyra2vc0ban`
- `lyra2z`
- `neoscrypt`
- `phi2`
- `phi`
- `pipe`
- `polytimos`
- `skein`
- `skunk`
- `stellite`
- `tribus`
- `x16r`
- `x16s`
- `x17`
- `x21s`
- `x22i`

`-d`, `--device` List of comma-separated device IDs to use for mining. IDs are numbered `0,1`...,N - 1

`-h`, `--help` Print help information

`-i`, `--intensity` Mining intensity (`0` - `6`). For example: `-i N[,N]` (default: `6`)

`-o`, `--url` URL of mining pool

`-p`, `--pass` Password/Options for mining pool

`-u`, `--user` Username for mining pool

`--log` Log output to file

`--no-color` Force color off

`--no-watchdog` Force watchdog off

`--no-crashreport` Force crash reporting off

`--cpu-priority` Set process priority in the range `0` (low) to `5` (high) (default: `3`)

`--api-type` Specify API type to use (default: `ccminer-tcp`)
- `ccminer-tcp` (TCP)
- `ccminer-ws` (WebSocket)
- `off`

`-b`, `--api-bind` IP:port for the miner API, `0` disabled (default: `127.0.0.1:4068`)

`-r`, `--retries` N number of times to retry if a network call fails, `-1` retry indefinitely (default: `-1`)

`-R`, `--retry-pause` N time to pause between retries, in seconds (default: `15`)

`--timeout` N network timeout, in seconds (default: `30`)

`-c`, `--config` JSON configuration file to use

## System Requirements

- <span style="color:#76b900">NVIDIA</span> GPUs with Compute Capability 5.0 or above
- Latest GeForce driver
- 2 GB RAM (4 GB recommended). Some algorithms such as NeoScrypt require the virtual memory (swap file) with the same size as all of the GPU's memory.
- Internet connection

### Windows

- Windows 7/8.1/10 (64-bit versions)
- [Visual C++ Redistributable for Visual Studio 2015](https://www.microsoft.com/en-US/download/details.aspx?id=48145)

### Linux

- Ubuntu 14.04+, Debian 8+ (64-bit versions)
- Package libc-ares2. Installing libc-ares2 package is as easy as running the following command on terminal: `apt-get install libc-ares2`

## Troubleshooting

### Antivirus Software Reports

CryptoDredge is not a piece of malicious software. You may try to add an exception in antivirus software you use.

### Rejected Shares

There are many reasons for rejected shares. The primary reasons are:
- high network latency
- overloaded mining server
- aggressive graphics card overclocking

### Watchdog

If you are using a third-party watchdog, you can disable the built-in watchdog by using `--no-watchdog` option.

Example:

```
CryptoDredge -a <ALGO> -o stratum+tcp://<POOL> -u <WALLET_ADDRESS> --no-watchdog
```

### Several Instances After a While

It seems that you are using an own restart mechanism of CryptoDredge (see the _Watchdog_ item).

### Crash Reporting

If the built-in watchdog is enabled then CryptoDredge will generate and send us the report. You can disable error reporting with `--no-crashreport` option. Allowing CryptoDredge to send us automatic reports helps us prioritize what to fix and improve in the future versions.

Crash reports won't include any personal information about you, but they might include:
- Operating System version
- Driver version
- Miner configuration
- Application crash data

## Contact

If you have problems, questions, ideas or suggestions, please contact us by posting to cryptodredge@gmail.com

## Web Site

Visit the CryptoDredge web site for the latest news and downloads: [https://cryptodredge.org/](https://cryptodredge.org/)
