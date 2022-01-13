Next, in my experiments of adopting more Web3 practices I looked into [unstoppabledomains](https://unstoppabledomains.com/).

### Domain Registration

I inferred that there is a solution in the works where the ownership of a domain would be stored on a blockchain; which sounded pretty cool! And I thought all my websites could be managed via domains purchased on this service.

It was not quite that. Yes, it does allow you to purchase a domain and have the domain resolve to your website; however the application/capability of unstoppabledomains were a lot more than that.

_For the scope of this article I will only talk about hosting and resolving your website on an unstoppabledomain_

If you are only wondering how the DNS resolution would work for a domain which resides on a blockchain and not on a www registry? Jump to the bottom of the article! (I wondered the same!)

### Hosting a Website using unstoppabledomains

Most of the steps involved are quite similar to the traditional way of hosting a website, however with a couple of key "Web3" differences :)

Steps

1. Create a website (static). Let's start with a simple "index.html" page
1. Purchase a domain on unstoppabledomains
1. Add and pin your index.html page onto IPFS (yes, this is one of key the differences)
3.1 Note down the IPFS hash for the index.html
1. Mint your domain
1. Link your domain using the IPFS hash (from earlier)
1. Enter your domain in the address bar of an unstoppabledomains browser. Or install the unstoppabledomains extension in your Chrome, Brave, etc (yes, this is the other key difference)

Let's dive into the points worthy of discussion.

### Pinning a file in IPFS

IPFS is a public file distribution/hosting protocol, where any node/machine connected to the IPFS network can make its file accessible to the outside world. You can easily setup your machine to be an IPFS node by running through a [simple ipfs setup](https://docs.ipfs.io/how-to/command-line-quick-start/#prerequisites).

_Additionally, IPFS allows it's nodes to host files temporarily or permanently (pinned)._

However, you might not be looking to host your website files on your own system, and the easiest way to have your website files pinned on the IPFS network is via a **pinning service**. e.g [pinata](https://www.pinata.cloud/), [infura](https://infura.io/product/ipfs), [eternum](https://www.eternum.io/)

### Linking the domain to an IPFS hash

On pinning your website files (or folder) to the IPFS network, you will receive an "IPFS hash". Mention this hash in the domain manager in upstopabledomains.

unstoppabledomains > my domains > manage domain "x" > website

![](https://gateway.pinata.cloud/ipfs/Qmdr8r1hFYrRxugPeK6WDe9pue4huDNN1Y7cq8LboZEQke)


### Accessing the website - Unstoppabledomains extension | Unstoppabledomains browser

Now coming to the last part of the puzzle which addresses how an end user can view your website on their web browser. 

Let's say the domain is "prakashraman.x", if a user where to type this in their traditional web browser, the chances are that no website would render. As the domain "prakashraman.x" does not resolve to any IP address in the hierarchy of DNS servers. 

So, now what? 

#### Browser
This leaves us in a situation where when there is no DNS entry which resovles "prakashraman.x" to an IP address. Therefore, this magic would need to happen right in the browser itself. 

The end users would need to use a browser which resolve unstoppabledomain domains to a IPFS accessible file. But do we have such a browser? Yes! And many of us are already using them - [Brave](https://brave.com/) and [Opera](https://www.opera.com/).

#### Browser Extension
unstoppabledomains have released [extensions](https://unstoppabledomains.com/extension) for Chrome and Firefox which can handle the domain resolution. 

Does this mean, for anyone to access your unstoppabledomains website would either need to install Brave, Opera or the extension? Yes, that would be needed indeed. Which might sound quite impractical, and yes, to an extent it would be. However as the world adopts and adapts to Web3 all browsers will (or should) start supporting unstoppabledomains resolutions. 

So until then, yes, I am definitely installing the extension AND using Brave as well!

This website is accessible via https://prakashraman.x 😊
