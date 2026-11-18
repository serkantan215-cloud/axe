# axe

axe is experimental C++ software for a decentralized cryptocurrency. It lets users send and receive payments over a peer-to-peer network, where participants collectively manage transactions and currency issuance rather than relying on a central authority.

## Features

- Send and receive cryptocurrency payments through a peer-to-peer network.
- Validate transactions and maintain a local copy of the blockchain.
- Check changes with C++ unit tests and Python regression and integration tests.

## Installation

Build from the project root on a Unix-like system. Install a C++ compiler, Make, Autotools, and pkg-config first, along with the development libraries required by the build. Dependency package names vary by operating system; resolve any missing dependencies reported by `configure` before continuing.

```sh
./autogen.sh
./configure --without-gui
make
```

The resulting command-line binaries are available in `src/`; a system-wide installation is not required.

## Usage

Start the node in the background:

```sh
./src/axed -daemon
```

The node connects to peers and begins synchronizing the blockchain. Synchronization requires network access, disk space, and time.

Check synchronization status:

```sh
./src/axe-cli getblockchaininfo
```

Stop the node cleanly:

```sh
./src/axe-cli stop
```

To run the unit tests after building:

```sh
make check
```

With the Python test dependencies installed, run the functional tests:

```sh
test/functional/test_runner.py
```

This is experimental, security-critical software. Test changes carefully before using them with funds.

## License

axe is released under the MIT license and is based on [AXErunners/axe](https://github.com/AXErunners/axe). See [COPYING](COPYING) for the license text and upstream copyright notices. Preserve those notices when redistributing the software or substantial portions of it.
