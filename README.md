# BTDEX - BlockTalk Decentralized Exchange reference client

![](https://github.com//btdex/btdex/workflows/BTDEX%20Build/badge.svg)
[![GPLv3](https://img.shields.io/badge/license-GPLv3-blue.svg)](LICENSE)

BTDEX is a decentralized exchange system running on the [Burst](https://www.burst-coin.org/) blockchain.
It implements a unique non-custodial exchange method for cryptocurrencies and conventional fiat currencies based on [BlockTalk](https://github.com/jjos2372/blocktalk) Smart Contracts and Burstcoin on-chain encrypted messages.
The exchange method is serverless and fees are distributed among [Trade Token (TRT)](https://explore.burstcoin.ro/asset/12402415494995249540) holders.

BTDEX is currently on *initial token distribution*, more details at [https://btdex.trade](https://btdex.trade).

## Download

Check the [releases](https://github.com/btdex/btdex/releases) and get the latest one.

### Running on Windows
Just download the `btdex-version.exe` [latest release](https://github.com/btdex/btdex/releases) and copy it
to a folder you have write rights (it will create a file named `config.properties` with your account details).
Double click on `btdex-version.exe` to start the application.

### Running on Linux

#### Ubuntu and other Debian-based distributions
Just download the `btdex_version_all.deb` [latest release](https://github.com/btdex/btdex/releases) and install it.
The application `BTDEX` will be available on the system (config file will go to `.config/btdex/` inside your home folder).

#### Archlinux
A package is available at [AUR](https://aur.archlinux.org/packages/btdex/).

### Running on MacOS
Just download the `btdex-mac-version.zip` [latest release](https://github.com/btdex/btdex/releases) and uncompress the app.
You can now run the app as usual (it will create a file named `config.properties` inside your home folder `~/`).

### General method without installing
Just download the `btdex-all-version.jar` [latest release](https://github.com/btdex/btdex/releases) and copy it
to a folder you have write rights (it will create a file named `config.properties` with your account details).
Run this jar file with Java 8 or more recent (the `xdg-utils` package is required to open your browser when necessary):

`java -jar btdex-all-version.jar`

## Translations
If you want to see BTDEX on your own language or have suggestions on how to improve a translation, please join us at https://www.transifex.com/btdex/.

## Compile from source

Clone this repository code and run the gradle build (requires Java 8 to build):

```
$ git clone https://github.com/btdex/btdex.git
$ cd btdex
$ ./gradlew shadowJar
```

This will result on the following file:

`build/libs/btdex-all.jar`

To build the windows executable run:

`$ ./gradlew createExe`

This will result on the following file:

`build/launch4j/btdex.exe`

## Running on testnet

Edit your `config.properties` file and add the following lines:

```
testnet=True
node=http\://testnet.getburst.net\:6876
```
## Logging

By default, logging turned off. Add/edit the following line to change logging level:

```
logging=off
```
### Logging level
Same logging level used to show log messages to console and save to file.<br><br>
OFF - The highest possible log level. This is intended for disabling logging.<br>
FATAL - Indicates server errors that cause premature termination. These logs are expected to be immediately visible on the command line that you used for starting the server.<br>
ERROR - Indicates other runtime errors or unexpected conditions. These logs are expected to be immediately visible on the command line that you used for starting the server.<br>
WARN - Indicates the use of deprecated APIs, poor use of API, possible errors, and other runtime situations that are undesirable or unexpected but not necessarily wrong. These logs are expected to be immediately visible on the command line that you used for starting the server.<br>
INFO - Indicates important runtime events, such as server startup/shutdown. These logs are expected to be immediately visible on the command line that you used for starting the server . It is recommended to keep these logs to a minimum.<br>
DEBUG - Provides detailed information on the flow through the system. This information is expected to be written to logs only. Generally, most lines logged by your application should be written as DEBUG logs.<br>
TRACE - Provides additional details on the behavior of events and services. This information is expected to be written to logs only.<br>

## License
[GPL license](LICENSE)

## Author
jjos

Donation address: BURST-JJQS-MMA4-GHB4-4ZNZU
