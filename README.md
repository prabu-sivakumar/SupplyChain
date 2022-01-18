# Building Supply Chain Decentralised App 

Building decentralised application for the Coffee Supply Chain use case. 

## UML Diagrams
The required UML diagrams are included in the UML folder. The UML diagrams are designed using Gliffy. 

## Libraries
|Library|Version  |
|--|--|
|Truffle  |v5.4.29 (core: 5.4.29)  |
|Solidity  |^0.4.24 (solc-js)  |
|Node  |v14.17.0  |
|Web3.js  |v1.5.3  |
|Truffle HD Wallet Provider  |1.0.17  |

## Configure version of Solidity in the truffle-config.js (Windows)
https://trufflesuite.com/docs/truffle/reference/configuration.html

```javascript
var  HDWalletProvider = require("truffle-hdwallet-provider");
const  fs = require('fs');
const  mnemonic = fs.readFileSync(".secret").toString().trim();
module.exports = {
	networks: {
		development: {
			host:  "127.0.0.1",
			port:  9545,
			network_id:  "*"
		},
		rinkeby: {
			provider:  function () {
				return  new  HDWalletProvider(mnemonic, "https://rinkeby.infura.io/v3/4db5346c3f2e45f4b7d3feee19595f83");
			},
			network_id:  4,
			gas:  4500000,
			gasPrice:  10000000000,
		}
	},
	compilers: {
		solc: {
			version:  "^0.4.24"
		}
	}
};
```

## Deploy Smart Contract to Public Test Network (Rinkeby)

If truffle is not installed, 

    npm install -g truffle

Install packages and required dependencies

    npm install

Compile Smart Contracts using Truffle 

    truffle dev

Create an Infura Project and copy the Rinkenby Endpoints. 
https://rinkeby.infura.io/v3/399cf7b9507d42848d7f954b3be2eba4

Create a .secret file and include the seed phrase used to connect to Metamask. 

    compile

Migrate Smart Contract to Rinkeby Test Network

    truffle migrate --network rinkeby

## Transaction ID and Contract Address

|ID| Value  |
|--|--|
|Transaction ID  |https://rinkeby.etherscan.io/tx/0x34a4b36a3e59574c3355a55a554a34be785963829108026e8f8adf7b551bdf7f   |
|Contract Address  |0x1dcbe6474c5e347ff289f1418f18be45b4f11d53  |
