# Vena Protocol

This repository contains the smart contracts source code for Vena Protocol. The repository uses Docker Compose and Hardhat as development environment for compilation, testing and deployment tasks.

🌐 **Website:** [https://www.vena.finance/](https://www.vena.finance/)

> **Note:** Vena Protocol is a fork of Aave V3, extended with reputation-based pricing mechanisms.

## What is Vena?

Vena is a reputation-priced liquidity protocol where capital has memory. Unlike traditional lending markets with flat rates, Vena adapts pricing based on reputation earned through past behavior and accountability.

### How Vena Works

**Reputation-Priced Liquidity**

Rates are not flat. They respond to reputation earned through past behavior and accountability. On Vena, capital prices trust, not anonymity.

**Reputation Through Prints**

Vena reflects reputation using Prints—an evolving signal built from repeatable actions, both onchain and offchain.

**Capital with Memory**

Good behavior compounds. Poor behavior decays. Pricing adapts as your reputation changes.

**Full Control by Default**

You control your assets through self-custody and your reputation through your actions.

## Documentation

Documentation for Vena Protocol is coming soon.

## Audits and Formal Verification

Security audits for Vena Protocol are planned prior to mainnet deployment.

## Setup

The repository uses Docker Compose to manage sensitive keys and load the configuration. Prior to any action like test or deploy, you must run `docker-compose up` to start the `contracts-env` container, and then connect to the container console via `docker-compose exec contracts-env bash`.

Follow the next steps to setup the repository:

- Install `docker` and `docker-compose`
- Create an environment file named `.env` and fill the next environment variables

```
# Add Alchemy or Infura provider keys, alchemy takes preference at the config level
ALCHEMY_KEY=""
INFURA_KEY=""


# Optional, if you plan to use Tenderly scripts
TENDERLY_PROJECT=""
TENDERLY_USERNAME=""

```

## Test

You can run the full test suite with the following commands:

```
# In one terminal
docker-compose up

# Open another tab or terminal
docker-compose exec contracts-env bash

# A new Bash terminal is prompted, connected to the container
npm run test
```
