Let's assume for a bit we have an incredible idea for a Dapp (because its so easy to come up with great app ideas!). 

It's typical for a Dapp to interact with blockchain. For this article let's consider a javascript Dapp that connects to the [Solana](https://solana.com/) network.

**Goal**: Successfully fetch the user's Solana address. 

## Ecosystem 

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

Solana offers a wallet adapter abstraction which internally supports various wallets, thus making it a little easier. 

### Step 1: Check if the wallet exists

```ts
import { PhantomWalletAdapter } from '@solana/wallet-adapter-wallets'

const wallet = new PhantomWalletAdapter()

wallet.readyState === "INSTALLED"
//Phantom wallet is installed in this browser"
```

### Step 2: Connect to the wallet and retrieve the public key/address

```ts
await wallet.connect();

wallet.publicKey.toString()

// A8WHmLMXHjQEb7VHjs4vu9B66NQNxrEDq2g84GmDGmhd
// yes, this is an address of mine on the solana devnet :)
```


And voila the Dapp is connected to the Solana network!

---

References: 

- https://github.com/solana-labs/wallet-adapter