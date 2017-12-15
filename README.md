# MiningSwitcher
This Java CLI application switches AltCoin Miners based on Current Profitability as found on WhatToMine.  
Currently only NVIDIA cards are supported.

## Currently Supported Miners
* CCMiner
* Ethminer
* further miners will be supported in a future release

## Currently Supported OS
* Linux
* Windows/MacOS/etc. may work as well (untested)

## System Requirements
* Java 1.8

## Dev Fee
* Approximately 1.6%
* It will mine for one minute to my wallet each hour
* I know it is rather easy to circumvent this dev fee, but I ask you to please not do so.

## Instructions

### Getting the executable JAR file and the config file
Download/Clone the Repository

### Setting up the configuration file
* Specify the number of NVIDIA cards you have
* For each coin make a new section under config (indentation important)
* Currently supported Coins: Ethereum, Vivo, Trezarcoin, Monacoin, Sibcoin, Vertcoin, Hush, Zencash, BitcoinGold, Orbitcoin, Feathercoin, Altcommunity, Pirl, LBRY, Zcash, Zclassic, Musicoin, EthereumClassic, PascalLite, Metaverse, Ubiq, Halcyon, GroestlCoin, Expanse, Electroneum, Decred, Karbowanec, Pascalcoin, Komodo, Soilcoin, Monero, Sumokoin, Bytecoin, Sia, DGB-Groestl, Myriad-Groestl, DigitalNote
* _miner_ is either CCMINER or ETHMINER
* _executablePath_ is the absolute path to the ccminer/ethminer executable
* _algorithm_ (relevant for ccminer only) is the algorithm to use, see ccminer --help
* _poolUrl_ is the pool URL without the port number
* _poolPort_ is the pool port
* _workerName_ is the name of the worker (or wallet address)
* _workerPassword_ is the worker password

### Running the program
```bash
    $ java -jar MiningSwitcher-0.0.1-SNAPSHOT-jar-with-dependencies.jar -c /path/to/config/MinerSettings.yaml
```
  
### Commandline arguments:
* -c (--config=)     Specify the path to the configuration file
* -d (--duration=)   Specify the duration between profitability checks in minutes
* -s (--select=)    Specify a coin to mine directly
