# Celo Dapp Greeter

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

Copy the address and request Alfajores testnet tokens from [Celo Faucet](https://celo.org/developers/faucet) 
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
You can also check the transaction on Celo-explorer, just click on the Smart-contract address in your front-end.

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

