RAPTURE Node
============

A RAPTURE full node for building applications and services with Node.js. A node is extensible and can be configured to run additional services. At the minimum a node has an interface to RaptureCore for more advanced address queries. Additional services can be enabled to make a node more useful such as exposing new APIs, running a block explorer and wallet service.

## Install

```bash
npm install -g bitcore-node-rapture
```

## Prerequisites

- RAPTURE Core with support for additional indexing *(see above)*
- Node.js v0.10, v0.12, v4 or v5
- ZeroMQ *(libzmq3-dev for Ubuntu/Debian or zeromq on OSX)*
- ~20GB of disk storage
- ~1GB of RAM

## Configuration

Bitcore includes a Command Line Interface (CLI) for managing, configuring and interfacing with your Bitcore Node.

```bash
bitcore-node-dash create -d <rapture-data-dir> mynode
cd mynode
bitcore-node-rapture install <service>
bitcore-node-rapture install https://github.com/yourname/helloworld
bitcore-node-rapture start
```

This will create a directory with configuration files for your node and install the necessary dependencies.

Please note that RaptureCore will be downloaded automatically. Once completed the dashd binary should be placed into the rapture-data-dir folder specified during node creation.

For more information about (and developing) services, please see the [Service Documentation](docs/services.md).

## Add-on Services

There are several add-on services available to extend the functionality of Bitcore:

- [Insight API](https://github.com/dashpay/insight-apirapture/tree/master)
- [Insight UI](https://github.com/dashpay/insight-uirapture/tree/master)
- [Bitcore Wallet Service](https://github.com/RaptureCore/bitcorewallet-service/tree/master)

## Documentation

- [Upgrade Notes](docs/upgrade.md)
- [Services](docs/services.md)
  - [Bitcoind](docs/services/bitcoind.md) - Interface to Bitcoin Core
  - [Web](docs/services/web.md) - Creates an express application over which services can expose their web/API content
- [Development Environment](docs/development.md) - Guide for setting up a development environment
- [Node](docs/node.md) - Details on the node constructor
- [Bus](docs/bus.md) - Overview of the event bus constructor
- [Release Process](docs/release.md) - Information about verifying a release and the release process.

## Contributing

Please send pull requests for bug fixes, code optimization, and ideas for improvement.

## License

Code released under [the MIT license](https://github.com/bitpay/bitcore-node-dash/blob/master/LICENSE).

Copyright 2013-2018 BitPay, Inc.

- bitcoin: Copyright (c) 2009-2018 Bitcoin Core Developers (MIT License)
