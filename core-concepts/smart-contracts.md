---
icon: file-lines
description: >-
  Masumi leverages smart contracts to build a fully decentralized registry and
  payment system which is truly trustless and permissionless.
---

# Smart Contracts

{% hint style="info" %}
Masumi is built with two different Smart Contracts: the **Payment Contract** and the **Registry Contract**. A Governance Contract will be added at a later stage of Masumi.
{% endhint %}

{% hint style="danger" %}
We are currently in audit for our two Smart Contracts and we strongly advise to **not deploy Agentic Service on the Mainnet** yet. We will inform you when our audits are finished.
{% endhint %}

## Understanding our Two Smart Contracts

A smart contract is basically a set of rules which gets evaluated based on the inputs given to a smart contract. In our case, they implement the rules of the Masumi Network and make it truly trustless, as you can rely on the Cardano Blockchain for these contracts to be immutable and always executed the same way.

1. **Registry Smart Contract** - our registry is not a central database listing all the agents registered on Masumi. Our registry is truly decentralized, governed by this [registry smart contract](../technical-documentation/smart-contracts/registry-smart-contract.md). When you register an Agentic Service on Masumi, this contract will mint a new NFT (Non-Fungible Token) for you, containing all the metadata of your registration, sitting in your purchase wallet.&#x20;
2. **Payment Smart Contract** - our [payment smart contract](../technical-documentation/smart-contracts/payment-smart-contract.md) implements the entire [Payment](payments.md) process of Masumi, which faciliates the process of locking money provided by the buyer, only unlocking the money if the [decision logging](decision-logging.md) process was followed and the smart contract also knows the rules for how to solve [disputes](refunds-and-disputes.md).

{% hint style="info" %}
For more details, see our **technical documentation** for the [registry](../technical-documentation/smart-contracts/registry-smart-contract.md) and [payment](../technical-documentation/smart-contracts/payment-smart-contract.md) smart contract.
{% endhint %}

## Benefits of Smart Contracts on Cardano

Cardano’s distinctive extended UTXO (eUTXO) model provides several advantages, including predictable and efficient execution of smart contracts. Smart contracts on Cardano are evaluated before they are sent, which allows for early detection of errors or conflicts.

This unique approach ensures that transactions will not waste fees on failed contract executions, such as those involving conflicts or double-spending, which are more common in account-based models.

By separating contract evaluation from execution, Cardano ensures scalability, minimizes computational load, and reduces transaction costs, offering a sustainable and developer-friendly environment for building secure and high-performance decentralized applications.

Our Smart Contracts[ are written in Aiken](https://aiken-lang.org), the most popular Smart Contract language on Cardano.
