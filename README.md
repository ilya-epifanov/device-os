[![Build Status](https://travis-ci.org/zsup/firmware-rust.svg?branch=feature/rust)](https://travis-ci.org/zsup/firmware-rust)

This repository is a starting point for incorporating Rust as a supported language for writing firmware applications on Particle devices (Core, Photon, and Electron).

Once this repository has been built out and has some level of stability, it will be merged into the [Particle firmware repo](https://www.github.com/spark/firmware).

## Getting started

- Install the latest Nightly build of Rust - https://www.rust-lang.org/downloads.html
- find the commit hash of the rust compiler:
```
$ rustc -v --version
rustc 1.7.0-nightly (4405944b9 2016-01-11)
binary: rustc
commit-hash: 4405944b9414d9d39d98c988c420b77e93acba96
commit-date: 2016-01-11
host: x86_64-apple-darwin
release: 1.7.0-nightly
``` 
- git clone https://github.com/rust-lang/rust
- checkout the commit listed above:
 - `git checkout <commit>`
- in this firmware repo, rebuild the core library for your specific version of the compiler
```
cd build/arm/rust
./build-core.sh <path-to-rust-repo>
```
- Build and flash the system modules (Photon/Electron)
- Build the default app  (rust blinky) just as you normally would
```
cd main
make PLATFORM=photon all program-dfu
```

## Project status

This project is currently a proof of concept. We are seeking contributors and a maintainer to drive this project forward, with heavy support from the Particle team. If you are interested in joining as a contributors or taking on the role of maintainer, please [join the discussion on our forums.](http://community.particle.io/t/rust-on-particle-call-for-contributors/19090)

### CREDITS AND ATTRIBUTIONS

The firmware uses the GNU GCC toolchain for ARM Cortex-M processors, ARM's CMSIS libraries, STM32 standard peripheral libraries and Arduino's implementation of Wiring.

On the Core: TI's CC3000 host driver libraries,
On the photon: Broadcom's WICED WiFi SDK.

### LICENSE

Unless stated elsewhere, file headers or otherwise, all files herein are licensed under an LGPLv3 license. For more information, please read the LICENSE file.

### CONTRIBUTE

If you are interested in joining as a contributors or taking on the role of maintainer, please [join the discussion on our forums.](http://community.particle.io/t/rust-on-particle-call-for-contributors/19090)

### CONNECT

Having problems or have awesome suggestions? Connect with us [here.](https://community.particle.io/)
