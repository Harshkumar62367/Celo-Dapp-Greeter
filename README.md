# Celo Progressive Dapp Starter

## Harsh (0x71B8937A0857Ea95aB41aa3007fE509D879D45f6) Documentation.

## How to Start the Dapp:

Prerequisites:

1. Node (v12), [NVM](https://github.com/nvm-sh/nvm) - will only work with Node v12, and not with Node 16.
2. Yarn
3. Git

Step 1:

```shell
git clone https://github.com/Harshkumar62367/Celo-Dapp-Greeter.git
```

Step 2:

```shell
cd Celo-Dapp-Greeter
nvm use  12 # uses node v12 as specified in .nvmrc
```

Step 3:

Open the project folder in Your favourite Ide.

Step 4:

Run these commands to install dependencies of Hardhat.

```shell
cd packages/hardhat
yarn install
```

Step 4:

Create a Hardhat-acccount and use your private key to add the account on Metamask

```shell
npx hardhat create-account
```
Add the private key to your Metamask wallet.

Step 5:

Copy the address and request testnet tokens from [Celo Faucet](https://celo.org/developers/faucet)
![image](https://user-images.githubusercontent.com/72465090/200105770-b90280ef-0731-40a3-a451-d542f2147ba7.png)

Step 6:

Create a .env file in Packages/Hardhat, and your PRIVATE_KEY there:

```shell
PRIVATE_KEY=" "
```

Step 7:
Once the TestTokens-received, Deploy the Contract:

```shell
yarn deploy
```

Once Deployed, terminal will show something like this:

```shell
Solidity compilation finished successfully
deploying "Greeter" (tx: 0x02ef05076d8a44b72291a12519a9bbcdebce36e5c34bb730cd83282abc9a1aac)...: deployed at 0x6E225b956857f65347b7deD2F25bCB3921a96AF7 with 530700 gas
deploying "Storage" (tx: 0x34ffd48553cdcaa7479b07f373c24e4fa88e1e7810a1c0cbc71b71b841d53602)...: deployed at 0xf95dD1F827e9459eB84B334DcEceF6523DFB0e12 with 179869 gas
Done in 35.89s.
```

<strong>You can also cross-check the Deployed-contract on Celo-Explorer to check my depoyed Greeter and Storage Contract.</strong>

Step 8:

Now move the folder to react app, to deploy our front-end to interact with our Smart-contract.

```shell
cd ../react-app
yarn install
```

Step 9:

Run yarn dev to start your development environment

```shell
yarn dev
```

Step 10:

Open localhost:3000 to view your project.

<b> It will look something like this</b>:

![image](https://user-images.githubusercontent.com/72465090/200106239-4445a134-7dce-4e88-8235-826bc745eb3b.png)
<br>
![image](https://user-images.githubusercontent.com/72465090/200106247-06964e8e-d913-4b52-b990-b66b04dc5cf3.png)

<strong> Notice our Smart Contract- Deployed Addresses in Our LocaHost-Dapp. </strong>

### Hurray! Your First-Dapp is Deployed now 🥳

Step 11:

Interact with the front-end to deploy or call our smart-contract:

![image](https://user-images.githubusercontent.com/72465090/200106583-7b349476-ab3b-4cea-bcaf-6eb9afbcd3b6.png)
<br>
![image](https://user-images.githubusercontent.com/72465090/200106609-3a8d28da-42b8-48d0-af79-1a85273eee68.png)
 
<br>
You can also check the transaction on Celo-explorer, just cick on the Smart-contract address in your front-end.

![image](https://user-images.githubusercontent.com/72465090/200106670-e0d6853f-1703-486f-b599-d3e3162ea109.png)


Step 12:

View on Mobile: Run this command to view your Dapp on mobile.

```shell
npx localtunnel --port 3000
```

Read more about locatunnel [here](https://www.npmjs.com/package/localtunnel).

Step 13:

You can further customize the Dapp by changing the front-end and adding more functionalities to the Dapp.


### If encountered any problem yoy can check this Official Celo Documentation [here](https://developers.celo.org/build-celo-dapps-in-15-minutes-or-less-438ea954d0b1).



<br>
<br>
<br>

## Official Documentation

A starter pack to get started with building dapps on Celo.

You can view a live version of the template deployed at https://celo-progressive-dapp-starter.netlify.app/.

This repo is heavily inspired by [scaffold-eth](https://github.com/scaffold-eth/scaffold-eth).

Prerequisites:

1. Node (v12), [NVM](https://github.com/nvm-sh/nvm)
2. Yarn
3. Git

```shell
git clone https://github.com/celo-org/celo-progressive-dapp-starter
```


## Intro Video

[![Intro Video](https://img.youtube.com/vi/MQg2sta0lr8/0.jpg)](https://youtu.be/MQg2sta0lr8)

## Using the Dapp Starter

### Set the correct node version (several Celo packages require using node version 12.x):

```shell
cd celo-progressive-dapp-starter
nvm use # uses node v12 as specified in .nvmrc
```

### Get testnet funds and install dependencies

```shell
cd packages/hardhat
yarn install
npx hardhat create-account # prints a private key + account
```

Paste the private key in `packages/hardhat/.env` and fund the account from the faucet [here](https://celo.org/developers/faucet). Once the account is funded, deploy the contracts with:

```shell
yarn deploy
```

Read more details about [the hardhat package here](packages/hardhat/README.md).

### In another terminal, start the frontend (React app using [Next.js](https://nextjs.org/))

```shell
cd packages/react-app
yarn install
yarn dev
```

### Testing on Mobile

- Get the Alfajores Testnet mobile wallet for Android and iOS [here](https://celo.org/developers/wallet).
- Serve your React app to your mobile device for testing via a tunnel.

Next.js defaults to serving your app on port 3000, so point the tunnel there:

```shell
npx localtunnel --port 3000
```

Read more about localtunnel [here](https://www.npmjs.com/package/localtunnel).

### Review

- Edit smart contracts in `packages/hardhat/contracts`.
- Edit deployment scripts in `packages/hardhat/deploy`.
- Edit frontend in `packages/react-app/pages/index.tsx`.
- Open http://localhost:3000 to see the app.

You can run `yarn deploy --reset` to force re-deploy your contracts to your local development chain.

## Deploy Your DApp

This repo comes with a `netlify.toml` file that makes it easy to deploy your front end using [Netlify](https://www.netlify.com/). The `toml` file contains instructions for Netlify to build and serve the site, so all you need to do is create an account and connect your GitHub repo to Netlify.

## Developing with local devchain

You can import account account keys for the local development chain into Metamask. To print they private keys of the local chain accounts `cd /packages/hardhat` and run

```shell
npx hardhat devchain-keys
```

If you are working on a local development blockchain, you may see errors about `the tx doesn't have the correct nonce.` This is because wallets often cache the account nonce to reduce the number of RPC calls and can get out of sync when you restart your development chain. You can reset the account nonce in Metamask by going to `Settings > Advanced > Reset Account`. This will clear the tx history and force Metamask to query the appropriate nonce from your development chain.

**Note:** You can get a local copy of mainnet by forking with Ganache. Learn more about [forking mainnet with Ganache here.](https://trufflesuite.com/blog/introducing-ganache-7/index.html#1-zero-config-mainnet-forking)

## React library choices

The example UI in `packages/react-app` uses the [Next.js](https://nextjs.org/) React framework, and [use-contractkit](https://www.npmjs.com/package/@celo-tools/use-contractkit) Celo library to get you started with building a responsive, web3 DApp quickly. Feel free to use it as a reference and use whatever web3 packages you are familiar with.

## The Graph

**Using the Graph is not a requirement for building a web3 application. It is more of a convenience for when your application is reading a lot of data from a blockchain.**

I suggest only adding support for the Graph when you need it, avoid premature optimization.

The `/packages/subgraphs` directory includes an example subgraph for reading data from the example `Storage.sol` contract. The Graph is a blockchain data indexing service that makes it easier to read data from EVM blockchains. You can read more about how the Graph works and how to use it in the [README here](/packages/subgraphs/README.md).

## 🔭 Learning Solidity

📕 Read the docs: https://docs.soliditylang.org

- [Primitive Data Types](https://solidity-by-example.org/primitives/)
- [Mappings](https://solidity-by-example.org/mapping/)
- [Structs](https://solidity-by-example.org/structs/)
- [Modifiers](https://solidity-by-example.org/function-modifier/)
- [Events](https://solidity-by-example.org/events/)
- [Inheritance](https://solidity-by-example.org/inheritance/)
- [Payable](https://solidity-by-example.org/payable/)
- [Fallback](https://solidity-by-example.org/fallback/)

📧 Learn the [Solidity globals and units](https://solidity.readthedocs.io/en/v0.6.6/units-and-global-variables.html)

## Support

Join the Celo Discord server at https://chat.celo.org. Reach out on the dedicated repo channel [here](https://discord.com/channels/600834479145353243/941003424298856448).

## Contributing

We welcome contributions to this repository!

If you decide to try this out and find something confusing, consider opening an pull request to make things more clear for the next developer that comes through.

If you improve the user interface or create new components that you think might be useful for other developers, consider opening a PR.

We will happily compensate you for contributions. Anywhere between 5 and 50 cUSD (or more) depending on the work. This is dependent on the work that is done and is ultimately up to the discretion of the Celo Foundation developer relations team.

You can view the associated bounty on Gitcoin [here](https://gitcoin.co/issue/celo-org/celo-progressive-dapp-starter/2/100027610).

## Troubleshooting

For M1 Mac developers who have installed nvm using brew, the server may crash. To resolve this issue, take a look here at this [solution](https://stackoverflow.com/a/67254340)
