# CollecTez

![api](https://github.com/catsoap/collec-tez/workflows/api/badge.svg)
![dapp](https://github.com/catsoap/collec-tez/workflows/dapp/badge.svg)

## What is this ?

Project to play around tzip-12

See current status of implementations:

- https://gitlab.com/smondet/fa2-smartpy
- https://github.com/stove-labs/tzip-12

## Requirements

You need to have the following tools installed:

- yarn
- firebase-tools (optional, used for deployment)
- docker (used for contract development)

## How it works?

A **Makefile** provides some shortcuts to help you. Just run

```bash
$ make
```

to see a help menu.

### Installation

Run `make install`, this will install `api` and `dapp` projects

### Infra

Run `make infra-up` to lauch the sandbox and tools containers

### Sandbox

Some commands, like deploy requires the config to be changed from the default one, for this run `make sandbox-config`

### Contract

TZIP-12 implementation contracts are deployable with `make contracts-originate-tzip`  
Default network is sandbox, you can deploy to tesnet by adding `NETWORK=testnet`  
The `.env` file `FA2_ADDRESS` is automatically updated with the new address.

### Dapp Dev

Launch api with `make api-serve`

Then run `make dapp-start`

### Local URLs:

- dapp: http://localhost:3000
- firebase admin: http://localhost:4000
- explorer: http://localhost:9000

## Useful links

### Pytezos

https://pytezos.baking-bad.org  
https://medium.com/tezoscommons/testing-michelson-contracts-with-pytezos-513718499e93  
https://blog.aira.life/tezos-dont-forget-the-mother-console-fd2001261e50

### TZIP-12

https://gitlab.com/tzip/tzip/-/blob/master/proposals/tzip-12/tzip-12.md  
https://forum.tezosagora.org/t/implementing-fa2-an-update-on-the-fa2-specification-and-smartpy-implementation-release/1870  
https://medium.com/@matej.sima/tutorial-implementing-a-mini-token-contract-on-tezos-with-on-chain-callbacks-tzip-12-b04cf7ee2059
https://smondet.gitlab.io/fa2-smartpy/
