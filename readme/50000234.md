# BONK Token Tracker Bot with ZettaBlock API

## Introduction

 The BONK Tracker Bot is a program that allows you to interact with the Solana blockchain that fetches the BONK token metadata live using the ZettaBlock API right in the telegram bot by just writing a simple command. 
 
 The ZettaBlock API is a set of APIs that allows developers to access and interact with the Solana blockchain.

## Installation

Clone the repository and install the dependencies.

```bash
git clone https://github.com/TheDARKFURY/EarnWeb3DAO---ZettaBlockAPI.git
cd EarnWeb3DAO---ZettaBlockAPI
yarn install
```

## Config

Create a `.env` file in the root directory of the project. Copy the contents of `.env.example` into the `.env` file and fill in the values for the variables.

Example:
```
API_ID = 'YOUR_API_ID'
BOT_TOKEN = 'YOUR_BOT_TOKEN'
X_API_KEY = 'YOUR_X_API_KEY'
```

## Run

To start the bot, run the command below:

```bash
$ node index.js
```

## Learn How to configure and make your own Telegram Bot

Read the Blog here -> https://dev.to/soham/how-to-create-a-telegrambot-using-zettablock-graphql-api-lgl

