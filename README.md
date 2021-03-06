Bitcore Node Safecoin
============

A Safecoin full node for building applications and services with Node.js. A node is extensible and can be configured to run additional services. Additional services can be enabled to make a node more useful such as exposing new APIs, running a block explorer and wallet service.

## Explorer Guide
### Part 1. Safecoin with extended RPC functionalities
```bash
wget -qO- https://raw.githubusercontent.com/Fair-Exchange/bitcore-node-safecoin/master/installSafecoind.sh | bash
```
### Part 2. Latest Safecoin insight explorer = bitcore-node-safecoin with insight-api-safecoin and insight-ui-safecoin
```bash
wget -qO- https://raw.githubusercontent.com/Fair-Exchange/bitcore-node-safecoin/master/installExplorer.sh | bash
```
## Explorer service management

To stop the service, dial:
```
systemctl stop explorer
```
To start the service, dial:
```
systemctl start explorer
```
To restart the service, dial:
```
systemctl restart explorer
```
To view the service status, dial:
```
systemctl status explorer
```
You may find it convenient to view the logged messages directly in the CLI. (To stop viewing in the journal reader, press CTRL + C):
```
journalctl -lf -u explorer
```

## Install

```bash
git clone https://github.com/Fair-Exchange/bitcore-node-safecoin.git
cd bitcore-node-safecoin
npm install
bitcore-node start
```

## Prerequisites

- GNU/Linux x86_32/x86_64, or OSX 64bit *(for safecoind distributed binaries)*
- Node.js v0.10, v0.12 or v4
- ZeroMQ *(libzmq3-dev for Ubuntu/Debian or zeromq on OSX)*
- ~30GB of disk storage
- ~2GB of RAM

## Configuration

Bitcore includes a Command Line Interface (CLI) for managing, configuring and interfacing with your Bitcore Node.

```bash
bitcore-node create -d <bitcoin-data-dir> mynode
cd mynode
bitcore-node install <service>
bitcore-node install https://github.com/yourname/helloworld
```

This will create a directory with configuration files for your node and install the necessary dependencies. For more information about (and developing) services, please see the [Service Documentation](docs/services.md).

## Add-on Services

There are several add-on services available to extend the functionality of Bitcore:

- [Insight API](https://github.com/Fair-Exchange/insight-api-safecoin)
- [Insight UI](https://github.com/Fair-Exchange/insight-ui-safecoin)

## Documentation

- [Upgrade Notes](docs/upgrade.md)
- [Services](docs/services.md)
  - [Bitcoind](docs/services/bitcoind.md) - Interface to Bitcoin Core
  - [Web](docs/services/web.md) - Creates an express application over which services can expose their web/API content
- [Development Environment](docs/development.md) - Guide for setting up a development environment
- [Node](docs/node.md) - Details on the node constructor
- [Bus](docs/bus.md) - Overview of the event bus constructor
- [Release Process](docs/release.md) - Information about verifying a release and the release process.


## License

Code released under [the MIT license](https://github.com/bitpay/bitcore-node/blob/master/LICENSE).

Copyright 2013-2015 BitPay, Inc.

- bitcoin: Copyright (c) 2009-2015 Bitcoin Core Developers (MIT License)
