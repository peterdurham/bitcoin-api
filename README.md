# Bitcoin API using Bitcoin Core, Node.js, and Express

Express API for querying data from your Bitcoin node to build web applications.  
  
Sends HTTP requests to Bitcoin Core node using various RPC commands.

A full tutorial for this API can be found [here](https://medium.com/@peterjd42/build-your-own-bitcoin-api-using-node-js-and-bitcoin-core-251e613623db).

## Setup
To use the API first make sure to install Node.js ([here](https://nodejs.org/en/download/)) and Bitcoin Core here ([here](https://bitcoin.org/en/download)).

Clone this repo and add a .env file at the root level of your project. Replace the bitcoinuser and bitcoinpassword values with those in your Bitcoin configuration file (in Bitcoin Core under `Settings > Options > Open Configuration File` ).  
  
### .env:
```

RPC_USER=bitcoinuser
RPC_PASSWORD=bitcoinpassword
```
If they haven't yet been set, add the following entries to your bitcoin.conf and change both files (restarting bitcoin core) :  
  
### bitcoin.conf:
```
rpcuser=bitcoinuser
rpcpassword=bitcoinpassword
```

Next run

```
npm install
```
then
```
npm run server
```
to start the server.

View a test endpoint in the browser at 'localhost:4444/api/getblockchaininfo'

## Methods used
- getblockcount
- getbestblockhash
- getconnectioncount
- getdifficulty
- getblockchaininfo
- getmininginfo
- getpeerinfo
- getrawmempool
- getblockhash
- getblock
- getrawtransaction
- decoderawtransaction
