# 🪙 Crypto-Crowdfunding

A  fundraising application in the Web3 ecosystem. People can create campaigns and help them using cryptocurrencies. </br>

### 🌐 Live url: https://crypto-crowdfunding-client.vercel.app/  </br>

<img src='https://user-images.githubusercontent.com/94712001/208749957-a844f123-a3d9-4e6c-9987-4b46b65fa0da.png' alt='imagem'/>


## ❓ How to use it 

<ul>
  <li>First of all, make sure that you have the metamask wallet installed in your browser, if not,<a href='https://metamask.io/' _blank>click here to download</a>, and create an account.</li>
  <li>Turn on test network in your metamask</li>
  <li>Sign in on <a href='https://goerlifaucet.com/' _blank>Goerli Faucet</a>, paste your wallet address and send test ETH , this part it´s important, because we´re gonna work with fake money for a while, we don´t want to use real money yet.</li>
</ul>

### After completed the steps above, let´s install the project.

Follow the steps:

```
gh repo clone RobertoAthos/Crypto-Crowdfunding
```

In the Client and Blockchain folder

```
npm install
```

### After you get installed, we´re gonna set some important configurations.

In **Blockchain** folder , create a new **.env** file with your metamask private key:
> Dont forget to always put this type of information in an .env file, do not share your private wallet key with anyone.

```
PRIVATE_KEY = 'Secret key here'
```

In **hardhat.config.js** file, add the following code:
> In your case, we´re gonna clone the repository, create the hardhat.config.js file in your blockchain folder and paste the code below.

```
module.exports = {
  solidity: {
    version: '0.8.9',
    defaultNetwork: 'goerli',
    netWorks:{
      hardhat: {},
      goerli:{
        url: 'https://rpc.ankr.com/eth_goerli',
        accounts: [`0x${process.env.PRIVATE_KEY}`]
      }
    },
    settings: {
      optimizer: {
        enabled: true,
        runs: 200,
      },
    },
  },
};
```

### Done ! The application will be ready to run, enjoy it 😄.





