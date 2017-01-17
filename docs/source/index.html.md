---
title: API Reference

language_tabs:
  - shell

toc_footers:

search: false
---

# Introduction

INFURA provides the world with secure, stable, and scalable Ethereum nodes. These docs will help you take advantage of the features INFURA provides.

# Endpoints

INFURA uses TLS-protected endpoints for security and privacy.

If you're not sure which network to use, use Mainnet.

Network      | Description                                      | URL
-------------|--------------------------------------------------|-------------------------------------------------------------------
Mainnet      | production network                               | [https://mainnet.infura.io/](https://mainnet.infura.io/)
Ropsten      | test network                                     | [https://ropsten.infura.io/](https://ropsten.infura.io/)
ConsenSysNet | [ConsenSys](https://consensys.net/) test network | [https://consensysnet.infura.io/](https://consensysnet.infura.io/)

<aside class="notice">
Remember the "s" in "https".
</aside>

# Calling a JSON-RPC method

Submit an HTTP POST request in [JSON-RPC 2.0](http://www.jsonrpc.org/specification) format.

<aside class="notice">
Don't forget to include the "Content-Type" header.
</aside>

> Calling a JSON-RPC method

```shell
$ curl -X POST \
  -H "Content-Type: application/json" \
  --data '{"jsonrpc": "2.0", "id": 1, "method": "eth_blockNumber", "params": []}' \
  "https://mainnet.infura.io/"
{"jsonrpc":"2.0","result":"0x27a2d3","id":1}
```

# Supported JSON-RPC methods

INFURA supports a subset of Ethereum's JSON-RPC methods. Most of the unsupported methods have to do with private keys (they're your keys so they should be on your computer; INFURA never sees them).

If you try to use a method that is not on this list, you will receive a `405 Method Not Allowed` HTTP response.

* [web3_clientVersion](https://github.com/ethereum/wiki/wiki/JSON-RPC#web3_clientversion)
* [web3_sha3](https://github.com/ethereum/wiki/wiki/JSON-RPC#web3_sha3)
* [net_version](https://github.com/ethereum/wiki/wiki/JSON-RPC#net_version)
* [net_listening](https://github.com/ethereum/wiki/wiki/JSON-RPC#net_listening)
* [net_peerCount](https://github.com/ethereum/wiki/wiki/JSON-RPC#net_peercount)
* [eth_protocolVersion](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_protocolversion)
* [eth_syncing](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_syncing)
* [eth_mining](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_mining)
* [eth_hashrate](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_hashrate)
* [eth_gasPrice](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gasprice)
* [eth_blockNumber](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_blocknumber)
* [eth_getBalance](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getbalance)
* [eth_getStorageAt](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getstorageat)
* [eth_getTransactionCount](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gettransactioncount)
* [eth_getBlockTransactionCountByHash](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getblocktransactioncountbyhash)
* [eth_getBlockTransactionCountByNumber](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getblocktransactioncountbynumber)
* [eth_getUncleCountByBlockHash](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getunclecountbyblockhash)
* [eth_getUncleCountByBlockNumber](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getunclecountbyblocknumber)
* [eth_getCode](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getcode)
* [eth_sendRawTransaction](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_sendrawtransaction)
* [eth_call](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_call)
* [eth_estimateGas](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_estimategas)
* [eth_getBlockByHash](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getblockbyhash)
* [eth_getBlockByNumber](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getblockbynumber)
* [eth_getTransactionByHash](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gettransactionbyhash)
* [eth_getTransactionByBlockHashAndIndex](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gettransactionbyblockhashandindex)
* [eth_getTransactionByBlockNumberAndIndex](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gettransactionbyblocknumberandindex)
* [eth_getTransactionReceipt](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_gettransactionreceipt)
* [eth_getUncleByBlockHashAndIndex](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getunclebyblockhashandindex)
* [eth_getUncleByBlockNumberAndIndex](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getunclebyblockbumberandindex)
* [eth_getCompilers](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getcompilers)
* [eth_compileSolidity](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_compilesolidity)
* [eth_compileLLL](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_compilelll)
* [eth_compileSerpent](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_compileserpent)
* [eth_getLogs](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getlogs)
* [eth_getWork](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_getwork)
* [eth_submitWork](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_submitwork)
* [eth_submitHashrate](https://github.com/ethereum/wiki/wiki/JSON-RPC#eth_submithashrate)
* [shh_version](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_version)
* [shh_post](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_post)
* [shh_newIdentity](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_newidentity)
* [shh_hasIdentity](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_hasidentity)
* [shh_newGroup](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_newgroup)
* [shh_addToGroup](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_addtogroup)
* [shh_newFilter](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_newfilter)
* [shh_uninstallFilter](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_uninstallfilter)
* [shh_getFilterChanges](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_getfilterchanges)
* [shh_getMessages](https://github.com/ethereum/wiki/wiki/JSON-RPC#shh_getmessages)

# Choosing a client to handle your request

In some situations, you may want your request to be handled by a specific client (e.g. Parity). To request a specific client, include the `Infura-Ethereum-Preferred-Client` HTTP header in your request. Next, provide the client name in lowercase.

> Selecting a preferred Ethereum client

```shell
$ curl -i -X POST \
  -H "Content-Type: application/json" \
  -H "Infura-Ethereum-Preferred-Client: parity" \
  --data '{"jsonrpc": "2.0", "id": 1, "method": "eth_blockNumber", "params": []}' \
  "https://mainnet.infura.io/"
HTTP/1.1 200 OK
Server: nginx/1.10.0
Date: Wed, 09 Nov 2016 21:44:34 GMT
Content-Type: application/json
Transfer-Encoding: chunked
Connection: keep-alive
Allow: OPTIONS, POST
Access-Control-Allow-Headers: origin, content-type, accept
Infura-Ethereum-Client: parity 1.4.1

{"jsonrpc":"2.0","result":"0x27a280","id":1}
```

The response includes the `Infura-Ethereum-Client` header, which names the actual client and version that handled the request.

If you request a client or client that is not available, you will receive a `400 Bad Request` response.

## Available clients

Client                                   | Name
-----------------------------------------|---------
[Parity](https://ethcore.io/parity.html) | `parity`
[Geth](http://geth.ethereum.org/)        | `geth`
