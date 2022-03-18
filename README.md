# Blockchain Starter

![shubham-dhage-IlUq1ruyv0Q-unsplash](https://user-images.githubusercontent.com/13135088/158922104-f3467e3c-8e84-4b8e-892f-0ff4bee398a5.jpg)

Photo by <a href="https://unsplash.com/@theshubhamdhage?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Shubham Dhage</a> on <a href="https://unsplash.com/s/photos/ethereum?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>

## About

The `blockchain-starter` allows you to quickly create a private blockchain with 10 addresses and run a local network.

## How To

There are two steps to getting everything up and running:

### 1. Set Up The Blockchain

`blockchain-starter` sets up a private blockchain by creating a genesis block and generating 10 addresses.

The [genesis](https://github.com/DOkwufulueze/blockchain-starter/blob/master/lib/genesis) script is responsible for creating the genesis block and generating addresses (10 of them) that can be used within the blockchain. To execute the [genesis](https://github.com/DOkwufulueze/blockchain-starter/blob/master/lib/genesis) script, run:

```shell
yarn genesis
```

After running the `yarn genesis` command above, a `builds/` directory would be created within the `blockchain-starter`'s root directory with the following artefacts generated:

- `accounts/` containing accounts with the following details:
  - address: made up of 40 hexadecimal characters prefixed by `0x`
  - password: the password is `password`
- `db/` containing chain data, key store, etc
- the `genesis.json` file specifying the genesis block

### 2. Start The Network - Mining Enabled

There are 4 options available for starting the network with mining enabled for use with DApps like [eth-vue](https://github.com/DOkwufulueze/eth-vue), for example:

#### Option 1: Start The Network Without Unlocking Any Account

To start the network which has been initialised in [step 1 of How To](#1-set-up-the-blockchain), without unlocking any account, just run the [start-network](https://github.com/DOkwufulueze/blockchain-starter/blob/master/lib/start-network) script. You could do this using `yarn` too:

```shell
yarn start
```

#### Option 2: Start The Network With Accounts Unlocked

To start the network with two accounts unlocked, `0x2Abe38bB3Cb626bE1e69Cc3776c4c3EA2B1DCa73` and `0x2Abe38bB3Cb626bE1e69Cc3776c4c3EA2B1DCa73` for example, run the following with the accounts in a comma-separated string:

```shell
yarn unlock-accounts-start 0x2Abe38bB3Cb626bE1e69Cc3776c4c3EA2B1DCa73,0x2Abe38bB3Cb626bE1e69Cc3776c4c3EA2B1DCa73
```

#### Option 3: Start The Network With All Accounts Unlocked

To start the network with all accounts generated in [this step](#1-set-up-the-blockchain) unlocked, run the following:

```shell
yarn unlock-all-start
```

#### Option 4: Start The Network With Your Coinbase Unlocked

To start the network with just your coinbase unlocked, run the following:

```shell
yarn unlock-coinbase-start
```

> NOTE: the accounts generated in [step 1 of How To](#1-set-up-the-blockchain) can be imported into [MetaMask](https://metamask.io/) if you choose to.

### Unlocking Accounts Without Mining

In addition to unlocking accounts and mining, `blockchain-starter` provides ways to unlock any number of available accounts without mining. The subsections below show how to unlock accounts for the two cases (*selected accounts* and *all accounts*):

#### 1. Unlocking Selected Accounts

To unlock accounts like `0x2Abe38bB3Cb626bE1e69Cc3776c4c3EA2B1DCa73` and `0x2Abe38bB3Cb626bE1e69Cc3776c4c3EA2B1DCa73`, for example, simply run the following command with the accounts as a comma-separated string:

```shell
yarn unlock-accounts 0x2Abe38bB3Cb626bE1e69Cc3776c4c3EA2B1DCa73,0x2Abe38bB3Cb626bE1e69Cc3776c4c3EA2B1DCa73
```

#### 2. Unlocking All Accounts

To unlock all the accounts generated [in this step](#1-set-up-the-blockchain), run the following:

```shell
yarn unlock-all-accounts
```

## Note

All accounts passed to `yarn` for unlocking must have been generated in [step 1 of How To](#1-set-up-the-blockchain) for things to go smoothly.

**Please send bug issues you may encounter to [Issues](https://github.com/DOkwufulueze/blockchain-starter/issues)**

## Copyleft

![Copyleft](https://github.com/DOkwufulueze/blockchain-starter/blob/master/images/copyleft.png) 2020 Daniel Okwufulueze

## Licence

This Blockchain Starter is distributed under the [GNU GPL-3.0](https://github.com/DOkwufulueze/blockchain-starter/blob/master/LICENCE.md) licence.
