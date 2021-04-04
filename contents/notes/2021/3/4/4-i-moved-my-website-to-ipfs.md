Until now my goto cloud provider for static webapps were [Netlify](https://www.netlify.com/) or [Render](https://render.com/) (which internally deploys on AWS, GCP, etc) as it addressed my requirement from a infra/deployment toolchain element perfectly. 

Since the advent of working blockchain solutions and interest and efforts towards Web3.0, it was only time before we would have solutions for deploying professional webapps on a distributed network. And that time is here. I think this is a notable event in the life of Web3.0, particularly as it enables many of us to migrate our existing projects from traditional centralized organizations (e.g AWS, GCP, Azure, etc) over to a distributed network! 

### What is IPFS

[IPFS](https://ipfs.io/) is a distributed system for storing and accessing files, websites, applications, and data. [1]

It is a protocol and peer-to-peer network for storing and sharing data in a distributed file system. IPFS uses content-addressing to uniquely identify each file in a global namespace connecting all computing devices.[2]

### Why I moved my website to IPFS

Whether we accept it or not (even whether we like it or not) we are already in early stages of [Web3.0](https://medium.com/fabric-ventures/what-is-web-3-0-why-it-matters-934eb07f3d2b) and it's only a matter of time before the principles of Web3.0 become widely adopted and even required. 

Distributed computing and storage has always been fascinating to me. Just the thought that we could leverage the billions of personal computers sitting idle at home around the world, potentially even rewarding those computers (nodes) for choosing to help be pillars and building blocks in the Web3.0 network. Amazing! It's the way it should be! (:bows)

This blog, used to be deployed on Netlify, and since the time IPFS started to get more advanced and stable I was waiting to migrate my website over and to test it out, and see how different (if at all) would be experience be. 

And very importantly I choose to be part of the generation that help makes Web3.0 into production environments and in mission critical systems. 

### Fleek.co

Couple of weeks ago, I made the decision to move this website onto IPFS (and consequently [Filcoin](https://filecoin.io/)). I start playing around with the CLI and looking for ways to go about it. And quickly enough I came across [Fleek.co](https://fleek.co/)

Fleek.co is a service which allows for deployment of webapps on the IPFS network. It takes care of pinning content, versioning, custom domain management and other deployment related functionalities. 

### How to setup a site/webapp

If you are familiar with Netlify, Heroku, Render, then Fleek.co is no different! Fleek.co currently allows to connect Github repos (Gitlab and Bitbucket are coming soon ...), set the branch, build command and the directory to be published on to IPFS. And that's it! As simple as that.

Below is my configuration for this website

![Fleek Configuration](https://i.imgur.com/zW6MNsw.png)

**Did I have any issues?**

Maybe just a couple :) When I pushed to my git repo, the deploy got stuck a couple of time. I tried updating the site-name in the site configuration and domain showed a 404. But, these were easy to fix, by just redeploying and re-verifying my domain. And the live chat customer service replied pretty much immediately to explain the situation and to let me know that everything is just fine!

However, these minor issues are expected at such an early stage of this service. But very importantly, it works much better than I expected it to! I am extremely with happy with Fleek (and IPFS) and I don't plan to move away anytime soon!

### Distributed Computing?

While IPFS and Fleek work perfectly for distributed storage, and therefore can be a viable option for deploying small to large scale Javascript webapps. What about deploying an micro-service (e.g a rest API service)? The answer could be [Holochain](https://holochain.org/) 

If you read the [about me](https://www.prakashraman.info/pages/about-me.html) page you see that I am very bullish on Holochain.

All-in-all I am thrilled with all the innovation in this space and we can expected amazing and truly ground breaking products and services to come out in the very near future.

<hr>

<sub>
[1] [https://docs.ipfs.io/concepts/what-is-ipfs/#decentralization](https://docs.ipfs.io/concepts/what-is-ipfs/#decentralization) <br>
[2] [https://en.wikipedia.org/wiki/InterPlanetary_File_System](https://en.wikipedia.org/wiki/InterPlanetary_File_System)
</sub>