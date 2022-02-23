Let's assume for a bit we have an incredible idea for a Dapp (because its so easy to come up with great app ideas!). 

It's typical for a Dapp to interact with a blockchain. For this article let's consider a javascript Dapp that connects to the [Solana](https://solana.com/) network.

**Goal**: Successfully fetch the user's Solana address. 

_This article heavily uses the [@solana-labs/wallet-adapter](https://github.com/solana-labs/wallet-adapter) to interface with the Solana network and wallets_

## Ecosystem 

![](https://gateway.pinata.cloud/ipfs/QmPcsXKok9ptyEqGvkVsASxaCByD7eeYDhnnySwA6A77LQ)

The following components/systems come into play for a Dapp to interact with the Solana Network

1. yourdapp.js
1. The desktop browser (yes, for now this needs to be on a Desktop)
1. Solana Wallet browser extension
1. your backend (optional)

## What Needs to Happen?

In order to retrieve the user's Solana address, the Dapp first needs to invoke the Wallet Browser Extension which in turn will ask the user if they want to share their address with the enclosing web application (Dapp)

Similar to an authentication flow of a SSO.

Pretty simple! When it comes down to it.

## Let's Understand the Workflow

Users can have multiple Solana Wallets (e.g [Phantom](https://phantom.app/), [Solfare](https://solflare.com/), etc) and, even though the Dapp only cares about retrieving a valid Solana address, it still needs to interact with a particular wallet (and therefore that wallet's API) to retrieve the address. 

Therefore, now, the Dapp would need to write wallet specific code. Yeah, it seems a little tedious and impractical as we don't know which wallet the user would have installed in the browser. 

Solana offers a [wallet adapter](https://github.com/solana-labs/wallet-adapter) abstraction which internally supports various wallets, thus making it a little easier. 

### Step 1: Check if the wallet exists

```ts
// yourdapp.js

import { PhantomWalletAdapter } 
    from '@solana/wallet-adapter-wallets'

const wallet = new PhantomWalletAdapter()

wallet.readyState === "INSTALLED"
//Phantom wallet is installed in this browser"
```

### Step 2: Connect to the wallet and retrieve the public key/address


When the browser executes the below line `wallet.connect()` it will open the Phantom Chrome Extension asking the user to give permission to the enclosing web application to retrieve its information.

```ts
// yourdapp.js

...
await wallet.connect();
wallet.publicKey.toString()

// A8WHmLMXHjQEb7VHjs4vu9B66NQNxrEDq2g84GmDGmhd
// yes, this is an address of mine on the solana devnet :)
```

### Step 3: Operate on the public key

Now your Dapp has the user's address, it can store it locally or can send the address to its backend and do what it wants with it! Maybe airdrop some SOL to it! :D

And voila the Dapp is connected to the Solana network!


## Question!

**Does this mean every user on the internet must install and maintain a Solana wallet to use the Dapp?**

Well if the Dapp connects to a Solana network then yes! But the considerations would be larger than that. Does the Dapp need to connect to a blockchain (i.e. Solana)? Does it need to run on a browser? Does it need user blockchain addresses?

If the answer to the above is Yes, then, yes, users would need to have a wallet installed on the browser they use at the time they open your Dapp. 

If you are thinking it does not seem that easy to use, you're right, it's not. However, the web3 ecosystem is growing and the interfaces into the web3 infrastructure is getting more native and inbuilt into the existing software we use daily.

_We might indeed be earlier to the game. But hell, as long as we are in the game, the timing will always be right!_

---

References: 

- https://github.com/solana-labs/wallet-adapter
- https://phantom.app/
- https://solflare.com/