# FAQ - Mining

## How to get started as a miner?

You will need to setup mining machine then, follow the steps in the [mining guide for the current epoch](https://www.youtube.com/playlist?list=PLOhw_qkI0ILWh5HDI8ZiFARjfkfvNPqev).

## Do I need a Raspberry Pi to mine?

Currently, all mining is simulated as we’re on testnet. When mainnet launches, the TEA Project will require mining machines that have TPM chips on-board and run a specially designed NixOS. At this early stage, you cannot use your existing PC for mining even though your PC already has a TPM chip on the motherboard. 

When mainnet starts, only AWS Nitro will be the first approved mining machines. Mining with a customized Raspberry Pi is on our roadmap for after mainnet launches, but there's no ETA on when that will be.

## What can I do with a CML?

CML is an NFT of the TEA Project that serves as a mining license. When users choose your CML node to host a TApp they want to use, you'll earn revenue in the form of the gas fee the end-user pays to run the TApp on your node.

Note that after planting into a mining machine, each CML will have a life span of approximately 2 weeks during the testnet epochs. This is an accelerated schedule specifically for the testnet as mainnet CML will have a lifespan of approximately 2 years.

## Why isn't my planted CML listed on wallet.teaproject.org?

There might be many reasons, but first make sure you followed all the instructions. One step that's sometimes missed is the "create entity" step after you plant your CML. If you don't create an entity, there's no way to pay you. Your entity is similar to a company owned by you that accepts your clients' payments.

## Why does my planted CML have a "pending" status?

Your node is in pending status because other TEA nodes have tried and failed in contacting your node to verify its integrity. This process is called "remote attestation", or RA for short. There might be many reasons that cause it to fail. The most common reason is that your server ports are not open to the public internet. We have a [troubleshooting guide](Mining-Required-Open-Ports.md) you can consult to help resolve this sort of issue. 

The solution may be simple or complicated. Some users mistakenly turn on Ubuntu Firewall (ufw), or it could be that your cloud service provider blocks all ports by default. Sometimes the fix is as simple as restarting the TEA docker services. But to find out you'll have to go step by step through the troubleshooting guide to diagnose the issue.

## How many CML will be launched on the mainnet?

There will be an nitial limit of 10k CML for the first two years after mainnet launch. The supply of CML will be controlled algorithmically by the DAO according to supply and demand after year 2. After the mainnet starts, the DAO will start to generate CML seeds and put them into the marketplace for auction.

## Do I need to do anything special to run RA?

RA (remote attestation) is mandatory for all TEA nodes. Anytime you run an active TEA node, it will run RA automatically. Of course, you'll get paid by running such a public service. There's no way for an active node to stop doing RA.

## Is there another option besides running CML nodes?

If you're not a technical person and don't how to navigate the linux command line, you can go to Harberger TApp to "rent" a **state maintainer seat**. You'll earn your income because the state maintainer nodes do the state maintaining work for the public, and you'll be the owner at least temporarily for as long as you're the high bidder for the seat.

## Can you elaborate on what kinds of services I can provide to earn TEA?

There are two kinds of services, public services and private services. Public services are paid by the DAO of the TEA Project. Those services benefit all members of our community, so we have to pay them from our DAO treasury or reserve account. The typical public service is RA (Remote Attestation). The RA is for public security, similar to security guards that protect commercial properties from crime. Since you cannot find a single payer for these kind of public services, the DAO will pay this fee.

"Private services" are a different kind of service that mostly run TApps or functions for community members (the endusers). Endusers will access your TEA node and run some code on it. It consumes your computing resources and the endusers pay you for using your node. Some of the private services are paid by the TApp owners (developers) instead of the enduser. This is common when the Tapp developers have some kind of business model to earn indirectly from endusers, e.g. advertisements. 

As long as you provide some kind of service, someone (DAO, end user, or tapp developer) will ultimately pay you.

## How are computing resources measured?

Similar to how Amazon calculates computing costs, we compute how much CPU instructions, memory usage, network traffic etc. are used during computational tasks. We've also learned from how Ethereum uses gas (such as using gas limits to prevent DDoS attacks) to provide safeguards in a decentralized compute environment. Generally speaking, the more complicated the task is that you run, the more you pay. If you don't have enough funds to pay at runtime, your task may be interrupted and dropped in the middle of execution.

## Can I move my CML license to a new machine?

You can move your CML license using the [CML transfer option](https://github.com/tearust/teaproject/wiki/CML-Migration-(Transfer)).
