# 🪙 Crypto-Crowdfunding

Uma aplicação de arrecadação de fundos estilo Vakinha Online no ecosistema da Web3. Pessoas podem criar campanhas e ajuda-las usando criptomoedas. </br>

### 🌐 Live url: https://crypto-crowdfunding-client.vercel.app/  </br>

<img src='https://user-images.githubusercontent.com/94712001/208749957-a844f123-a3d9-4e6c-9987-4b46b65fa0da.png' alt='imagem'/>


## ❓ Como usar

<ul>
  <li>Primeiro de tudo, tenha a carteira metamask instalada no seu browser, se não tiver, pode <a href='https://metamask.io/' _blank>Clicar aqui</a>, baixar e criar uma conta.</li>
  <li>Ative a rede de teste no seu metamask.</li>
  <li>Entre e faça login no site <a href='https://goerlifaucet.com/' _blank>Goerli Faucet</a>, cole seu endereço da carteira no input e envie eth para sua carteira, essa parte é bem importante, pois esses eth que você vai está enviando são criptos de teste.</li>
</ul>

### Após ter completado os passos acima, vamos a instalação do projeto.

Para instalar, siga estas etapas:

```
gh repo clone RobertoAthos/Crypto-Crowdfunding
```

Na pasta Client & Blockchain

```
npm install
```

### Depois de ter instalado, vamos para algumas configurações importantes no projeto.

Na pasta **Blockchain**, crie um arquivo **.env** com a chave privada da sua metamask:
> Não esqueça de sempre colocar esse tipo de informaçãoem um aquivo .env, não compartilhe com ninguém a sua chave privada da carteira.

```
PRIVATE_KEY = 'Cole sua private key aqui'
```

Em seguida, no arquivo **hardhat.config.js**, adicione o código abaixo
> No seu caso como vamos está clonando o repositório, crie esse arquivo hardhat.config.js na sua pasta blockchain e cole o código abaixo.

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

### E pronto ! A aplicação já vai está pronta, aproveite 😄.





