# Redstone Wallet

__Warning: We're currently testing, so use at your own risk.__  
This is the repository of the Redstone Wallet, a full node staking wallet using Electron and Angular at the front-end and .NET Core with C# in the back-end.

# Building and running the Redstone daemon

The Redstone daemon is the backend REST service, hosting a Redstone node upon which FullNode UI depends.  
The Redstone daemon is hosted in another repository. All information on building and running the daemon can be found [here](https://github.com/RedstonePlatform/Redstone/blob/master/Documentation/getting-started.md).

# Building and running the Redstone user interface

## Install NodeJS

Download and install the latest Long Term Support (LTS) version of NodeJS at: https://nodejs.org/. 

``` bash
wget https://nodejs.org/dist/v8.11.1/node-v8.11.1-linux-x64.tar.xz
sudo tar -xf node-v8.11.1-linux-x64.tar.xz
rm node-v8.11.1-linux-x64.tar.xz
```

## Getting Started

Clone this repository locally:

``` bash
git clone --recurse-submodules https://github.com/RedstonePlatform/Redstone-Wallet.git
```

Navigate to the StratisCore.UI folder in a terminal:
``` bash
cd ./Redstone-Wallet/StratisCore.UI
```

## Install dependencies with npm:

From within the StratisCore.UI directory run:

``` bash
npm install
```

## Run the UI in development mode

#### Terminal Window 1
[Run the daemon](https://github.com/RedstonePlatform/Redstone/blob/master/Documentation/getting-started.md)  

#### Terminal Window 2
Use `npm run mainnet` to start the UI in mainnet mode or `npm run testnet` to start the UI in testnet mode.  
This will compile the Angular code and spawn the Electron process.

## Build the UI for production

|Command|Description|
|--|--|
|`npm run build:prod`| Compiles the application for production. Output files can be found in the dist folder |
|`npm run package:linux`| Builds your application and creates an app consumable on linux system |
|`npm run package:linuxarm`| Builds your application and creates an app consumable on linux-arm system (i.e., Raspberry Pi) |
|`npm run package:windows`| On a Windows OS, builds your application and creates an app consumable in windows 32/64 bit systems |
|`npm run package:mac`|  On a MAC OS, builds your application and generates a `.app` file of your application that can be run on Mac |

**The application is optimised. Only the files of /dist folder are included in the executable. Distributable packages can be found in the StratisCore.UI/app-builds/ folder**


