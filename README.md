<!-- # Factom-FAQ

A list of frequently asked questions about the Factom protocol and governance -->

# General FAQ

### What is Factom?

Factom is an open-source, decentralised, public protocol that uses blockchain to establish data-integrity. Factom is a pure data blockchain: it offers a way to prove the existence and state of arbitrary data. Typical use cases include proof-of-existence, tokenisation, and smart contracts. Factom has a [two-token system](https://github.com/Factoshi/Factom-FAQ#how-does-factoms-two-token-system-work) designed to ensure predictable fees that allow businesses to use the blockchain for a predictable cost without handling cryptocurrency.

### Is Factom a public or private blockchain?

Factom can be used as both a public or a private blockchain. The information in this FAQ pertains to the public blockchain, though Factom Inc does have a private blockchain solution that they offer to clients, and there may be other businesses implementing/using a private version of Factom.

### What was M3?

Milestone 3, or M3, was the most recent major release of Factomd. It marked the point at which Factom transitioned from a centralised protocol developed and run exclusively by Factom Inc, to becoming a decentralised protocol operated and governed by dozens of companies worldwide. Furthermore, M3 marked the introduction of Factom's inflation mechanism, which is used to pay for decentralisation of the protocol and for other important development, marketing and infrastructure efforts via the [grant pool](https://github.com/Factoshi/Factom-FAQ#what-is-the-grant-pool).

### What is the difference between Factom and Factom Inc?

The Factom protocol is an open source data integrity protocol built by a coalition of technology companies that extends the security of blockchain to any type of data. Factom Inc., is the US company that conceived and initially developed Factom.

This is an important distinction, as there are many companies actively developing and writing applications for Factom.

# Blockchain and Protocol

### What is an Entry?

An Entry is an arbitrary piece of data that has been committed to the blockchain. An Entry on Factom is conceptually similar to making an entry in a physical ledger.

### What is an Entry Chain?

An Entry Chain is a discrete sub-chain created by a user to store Entries. This design allows users to organise and associate Entries. For example, if someone wants to track changes to a document over time, they would create a new Entry Chain specifically for that document.

An important function of Entry Chains is to allow users to efficiently prove a negative. If some data is absent from an Entry Chain, then it can be reasonably assumed to not exist. For example, if a user creates an Entry Chain to track a mortgage application and some dispute later arises over the state of that application, then the absence of an Entry showing that state in the mortgage application’s Entry Chain effectively shows that the state in question had never existed.

### What is anchoring?

Factom leverages the security delivered by Bitcoin’s proof of work in order to improve its own security. It achieves this by inserting the most recent directory block hash into Bitcoin using Bitcoin’s OP_RETURN feature. This process is known as “anchoring”.

Factom is blockchain-agnostic; it can anchor into any other blockchain. It currently only uses Bitcoin, but there is also work underway to integrate Ethereum as well.

### How does Factom's two-token system work?

Factom uses two tokens. The first is the Factoid (FCT). The Factoid is a transferrable (i.e. tradeable) token used as a means of value transfer on the network. Factoid inflation is used to pay Factom Authority Node Operators for decentralising the protocol and managing write-access to the blockchain. It is necessary to burn (destroy) Factoids to create the second of the two tokens, Entry Credits.

Entry Credits (EC) are a non-transferrable (i.e. non-tradeable) token used to pay for network use. They are created by burning FCT. Entry Credits are non-divisible units that can each pay for up to 1 kb of data storage on the Factom blockchain. Entry Credits are completely destroyed once they have been used; they are not transferred anywhere.

There is a variable exchange rate between FCT and EC. This exchange rate is determined by the network oracle, which is currently operated by Factom Inc. The purpose of the variable exchange rate is to always target a consistent cost of 1000 Entry Credits for \$1. Targeting a stable Entry Credit price allows businesses to accurately budget their use of the protocol.

Together, Factoids and Entry Credits create a 'mint and burn' system. The costs associated with the network are payed for in the minting process, and use of network resources ensure continuing demand of those tokens via their necessary destruction.

### What is meant when people say that Factom is "pure data"?

When people say that Factom is 'pure data', they mean that the content of entries do not contain any code to be executed on-chain. This is unlike other smart contract blockchains, where code is executed by every node on the network in order to update state. On Factom, smart contracts execute code off-chain. Only the resulting data - the state - is stored on chain.

# Authority Nodes

### What is an Authority Node?

An Authority Node is a network node that has sufficient privileges to write data onto the Factom blockchain. An Authority Node is a broad term that encompasses two different types of network node on Factom, federated nodes and audit nodes:

-   Federated nodes (AKA ‘Feds’ or ‘Leaders’) are nodes that actively write data into the blockchain. Federated nodes account for roughly half of authority nodes.
-   Audit nodes (AKA ‘audits’) are nodes acting on standby, ready to take the place of a federated node if it fails.

Federated nodes and audit nodes trade places in events known as ‘elections’. These elections are entirely automated on-chain events that require no human intervention.

All non-Authority nodes are referred to simply as 'followers'. These nodes have no special privileges in the network. They are used to download the blockchain and broadcast/relay new transactions.

### What is an Authority Node Operator?

An Authority Node Operator (ANO) is an organisation that operates the network’s [Authority Nodes](https://github.com/Factoshi/Factom-FAQ#what-is-the-grant-pool). Beyond that, ANOs are expected to also take part in governance and, depending on their [efficiency](https://github.com/Factoshi/Factom-FAQ#what-is-the-grant-pool), contribute meaningfully to marketing the protocol and/or software development (whether that be some application that uses Factom or core development).

### How are Authority Nodes Operators chosen?

Authority Nodes are chosen by [standing parties](https://github.com/Factoshi/Factom-FAQ#what-is-a-standing-party) in regular elections.

### What is efficiency as it pertains to authority node operators?

Each authority node can receive a maximum 1123 FCT per month for its service in securing and performing consensus on the network. Efficiency refers to the percentage of that payment that a server defers to the [grant pool](https://github.com/Factoshi/Factom-FAQ#what-is-the-grant-pool).

By deferring funds to the grant pool, an authority node operator increases their impact by ensuring that useful projects can receive funding. Conversely, by retaining funds, an authority node operator can typically use those funds to meet self-defined development or marketing goals.

High efficiency nodes are often referred to as “infrastructure nodes”, as their primary activity is typically to provide a stable network infrastructure.

# Governance

### What is a standing party?

A standing party is an entity that has some kind of provable vested interest or reputation in the protocol. Currently, standing parties include [Guides](https://github.com/Factoshi/Factom-FAQ#what-is-a-guide) and [Authority Node Operators](https://github.com/factoshi/factom-faq#what-is-an-authority-node-operator).

Eventually, standing parties will include Guides, Authority Node Operators, Factoid holders, Factoid burners and Entry Credit users. At that stage, all elections are expected to take place in a continuous on-chain process.

### What is a Guide?

A Guide is a [standing party](https://github.com/Factoshi/Factom-FAQ#what-is-a-standing-party) who drives forwards key protocol governance issues. They often introduce new governance legislation and are intimately involved in the finer details of protocol governance. There are currently 5 Guides. They have term lengths of one year and all Guides stand for election at the same time. Along with other standing parties, Guides cast votes on governance matters.

### Where can I read Factom's governance documents?

You can read more about Factom's formal governance processes on the [Factom Protocol website](https://factomize.com/forums/documents/)

# Business

### Who is using Factom?

Factom is used by a number of different private, public and charitable organisations, with many others reportedly in the pipeline. These include, but are not limited to:

-   [The Bill and Melinda Gates Foundation](https://www.youtube.com/watch?v=rf5lg6kEMEg)
-   [Equator](https://www.nasdaq.com/press-release/equator-launches-mortgage-servicing-blockchain-solution-20181113-00843)
-   [Linxens](https://www.linxens.com/dloc/)
-   [Blockchain-as-a-service company Sphereon](https://www.investinblockchain.com/sphereon-factom-first-live-customer/)
-   [Yooya](https://bitcoinexchangeguide.com/yooya-to-use-factom-harmony-blockchain-for-video-verification-in-china/)

and many others...

Factom Inc has won a series of grants from the US Department of Homeland Security to secure data generated by IoT border devices.

### What are Factom's use cases?

Factom has a number of use cases that can all be derived from its ability to establish robust data integrity:

1. Proof of existence - Committing some data or the hash of some data proves that data existed at the time the block was created.
2. Smart contracts - Computation takes place off-chain then new state is updated on-chain.
3. Tokenisation - An extension of smart contracts. See the [FAT Protocol](https://github.com/Factom-Asset-Tokens/FAT).
4. Digital Identities - A self-sovereign digital identity fully under the control of the end user.

Each of these core concepts can be expanded in many directions to be used by many different industries. For example, tokenisation might allow for the representation of physical objects on the Factom blockchain that can then be tracked and traded. Proof of existence can be used to prove that data existed at the timestamp of the block it is hashed into.

### Why do people say that companies do not need to use Entry Credits to use the protocol?

Factom is the basis of a number of blockchain-as-a-service offerings. These service companies provide an API for clients to commit data to the Factom blockchain. As part of that service, they also manage the cryptocurrency aspect for their clients. Though the client pays to use the blockchain, they do not need to handle any cryptocurrency - that is done on their behalf.

### What is the grant pool?

The grant pool is a pool of FCT use to fund grants designed to somehow advance the Factom ecosystem or pay for necessary infrastructure. Recent grants include development of the Factom Ledger Nano S application and development of the Factom Asset Token protocol. Core development is also funded via the grant pool.

The FCT in the grant pool is replenished by network inflation (see question on [efficiency](https://github.com/Factoshi/Factom-FAQ#what-is-efficiency-as-it-pertains-to-authority-node-operators)).

# Development

### Who develops the Factom protocol?

The vast bulk of core development on the Factom protocol has thus far been completed by Factom Inc. However, several other businesses have recently begun to contribute towards core development, and there are plans by others to begin work in the near future.

### What is factomd?

Factomd is the software that implements the Factom protocol. It downloads blocks, broadcasts transactions and, for authority nodes, also works to perform network consensus. Factomd has an API that lets other software interact with it programmatically.

### What is walletd?

Walletd is used to manage personal public/private keys. It builds and signs transactions, which are then broadcast using Factomd.
