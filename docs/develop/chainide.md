---
id: chainide
title: Using ChainIDE
sidebar_label: Using ChainIDE
description: Build your next blockchain app on Polygon.
keywords:
  - docs
  - matic
image: https://matic.network/banners/matic-network-16x9.png 
---

# Using ChainIDE

This is the beginner guide to creating and deploying a simple ERC-721 smart contract on Polygon Mumbai Testnet using ChainIDE, MetaMask, and Solidity. 
If you have any questions, feel free to join [ChainIDE Discord!](https://discord.gg/QpGq4hjWrh)

Following are the steps to deploy an ERC-721 smart contract:
1. Install MetaMask
2. Write down an ERC-721 smart contract
3. Compile the smart contract
4. Deploy the smart contract
5. NFT Minting
6. Create a flattened file for the smart contract verification
7. Verify the deployed smart contract on Polygonscan


### 1. Install MetaMask
When we deploy a smart contract on the blockchain or make a transaction to the deployed smart contract, we need to pay the gas fee, and for that. we need to have a Web3 wallet, which is MetaMask. So, first of all, we'll install MetaMask, 
please click [here](https://metamask.io/) to install MetaMask, and after installing, you need to add Polygon Mumbai Testnet to the MetaMask. To check how to add Polygon Mumbai Testnet manually to the MetaMask, please click [here](https://docs.polygon.technology/docs/develop/metamask/config-polygon-on-metamask#add-the-polygon-network-manually), and click [here](https://faucet.polygon.technology/) to get some dummy coins for the Mumbai Testnet.(or google "polygon faucet") 


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image.png)

### 2. Write down an ERC-721 Smart contract 

You need to write down all the required functions that you want to implement in your ERC-721 smart contract. A general ERC-721 smart contract has the following functions. 
 - balanceOf(): return by_ The number of NFTs held by the owner
 - ownerOf(): returns the address of the token holder
 - grant address_ To has_ Token ID control. Approval event needs to be triggered after the method is successful
 - setApprovalForAll(): Grant address_ The operator has the control of all NFTs, and the approvalforall event needs to be triggered after success
 - getApproved(), isApprovedForAll(): Used to query authorization
 - safeTransferFrom(): To transfer the ownership of NFT, a successful transfer operation must initiate a transfer event
 - transferFrom(): It is used to transfer NFTs. After the method succeeds, it needs to trigger the transfer event. The caller confirms himself_ To address can receive NFT normally, otherwise, this NFT will be lost. When this function is implemented, it needs to check whether it meets the judgment conditions

ChainIDE team has prepared the complete ERC-721 showcase including all the required functions, you may use that built-in template and add/delete functions according to your requirements.

Go www.chainide.com ,Click "Try Now"

![](https://3869740696-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-MYy-lqJKjq1m0yBAX4r%2Fuploads%2Fnpdf7fg51675wYmFcL6b%2Fimage.png?alt=media&token=353fc876-a319-49cb-92d5-1ed23c39aa90)

Then, click "New Project" and select "Polygon" , "ERC721 Showcase"

![](https://chainide-doc.s3.amazonaws.com/Using+ChainIDE+polygon/select+polygon+showcase.png)

Now, you can see Creature.sol including all the required functions.

After creating the project, click the unconnected button in the upper right corner, select the Injected Web3 Provider button, and select the Metamask wallet to connect to the Metamask wallet (Polygon Mainnet is the main network, and Mumbai is the test network). This time we connect to Mumbai.

![](https://chainide-doc.s3.amazonaws.com/Using+ChainIDE+polygon/connect+mumbai.png)

### 3. Compile an ERC-721 smart contract
After you have completed writing down your smart contract, 
it's time to compile the smart contract. 
To compile, please go to compile the module, choose an appropriate compiler according to your source code, 
and press compile button. After successful compilation, an ABI and byte code for the source code will be generated. 
If there are some errors in your source code, they would be displayed under the output panel in the Logger module. 
You may need to carefully read the error, resolve it accordingly and compile it again.
! Please note down the compiler version and the license for your source code as it would be needed when you verify your smart contract on the Polygon Mumbai Testnet.

![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(1).png)


### 4. Deploy an ERC-721 Smart Contract
After successful compilation, it's time to deploy your compiled ERC-721 smart contract to the Polygon Mumbai Test Network. 
For that, you need to have a MetaMask installed, Polygon Mumbai Test Network added to your MetaMask, 
and some dummy coins to pay for the transaction fee. 



You need to go to the "Deploy & Interaction" module and choose among the compiled smart contract, 
the smart contract you want to deploy and click the deploy button. 
For this tutorial, we'll use the "GameItem" smart contract to deploy.


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(2).png)

After the successful deployment, a message can be seen in the output section that your smart contract has been deployed successfully, 
and you can verify the deployed smart contract on the Polygon Mumbai Test Network too. All the functions in the deployed smart contract can be seen in the "INTERACT" panel.

![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(3).png)

### 5. NFT Minting
To mint an NFT, you need to use the award item function and use the wallet address of someone to whom you want to award an NFT,
 and the link of the photo uploaded to IPFS needs to be pasted in the token URL input field.


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(4).png)


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(5).png)


After successful minting, you can check the minted NFT on the OpenSea NFT marketplace. 
Visit [OpenSea Testnet](https://testnets.opensea.io/), connect your MetaMask wallet, and make sure the selected network is Polygon Mumbai Testnet, and you'll be able to see and trade the minted NFT on the OpenSea NFT marketplace.


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(6).png)

### 6. Create a Flattened File using Flattener Library
To verify a smart contract that imports other smart contracts, 
we need to create a flattened file, 
a flattened file including all the source code of imported contracts in a single file. 
To create a flattened file, you need to add a "Flattener" plug-in.


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(7).png)


Once the Flatterner plug-in is activated, you'll be able to access it as a separate module as shown in the figure below. 
Choose the compiled file, and click on the flatten button to create a flattened file, once the flattened file is created,
 it will be automatically copied to the clipboard, 
you may paste it to a file and save it for later usage.


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(8).png)


If you want to save the flattened file, click save button, and a flattened file will be saved in the current repository.


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(9).png)


The saved flattened file can be access under the explorer module.


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(10).png)

### 7.  Verify a Smart Contract
To verify a smart contract, you need to visit [Mumbai Polygonscan](https://mumbai.polygonscan.com/), and 
search for the deployed smart contract using the contract address.


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(11).png)


Click on the verify and publish link shown under the contract section. 


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(12).png)

Once you click on the verify and publish link, you will be asked for the following:

 - Contract Address: The address of a deployed smart contract that you want to verify
 - Compiler Type: Either you want to verify a single file or multiple files
 - Compiler Version: The compiler version that you used to compile the smart contract
 - License: Open-source license type that you used for your source code

![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(13).png)

After that, you  need to paste the flattened file that you created in step 5, and your smart contract will be verified. 

![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(14).png)

If there are no issues with your smart contract, it would be verified, and you'll be able to see an image similar to the one that is shown below.


![](https://chainide-doc.s3.amazonaws.com/ERC+721+Deployment+on++Mumbai/image+(15).png)


Your smart contract is verified, and you're done with this tutorial. 

 