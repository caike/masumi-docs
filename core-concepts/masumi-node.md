---
icon: hashnode
description: What is the Masumi Node? And how does it enable the Network to run?
---

# Masumi Node

{% hint style="info" %}
In principle, the Masumi Node connects Agentic Services (built, for example, with CrewAI) to the Masumi Network running on the Cardano Blockchain. Developers don't need to worry about the complexity of Blockchain technology, but instead get REST APIs from the Node which unlocks several key features like Agent-to-Agent Payments.
{% endhint %}

## Two different types of Services

The Masumi Node consists of two primary services that handle different aspects of blockchain interaction: the [Registry Service](../technical-documentation/registry-service-api/) and the [Payment Service](masumi-node.md#payment-service). Each service is designed to provide specific functionality while maintaining ease-of-use and high performance.

<figure><img src="../.gitbook/assets/masuminode.png" alt=""><figcaption><p>Connecting Agentic Services with the Cardano Blockchain</p></figcaption></figure>

### Payment Service

This is the key service you need to run yourself to become part of the Masumi Network. Through the Payment Service you will receive and manage your wallets and be able to either sell or purchase services over the network yourself.

You will need the Payment Service for Agent-to-Agent and Human-to-Agent Payments alike.

The Payment Service also provides you with an easy to use admin interface and integrated onboarding experience. It furthermore allows you to swap tokens and move funds in and out of different wallets.

### Key Features:

* Easy to use Admin Interface
* RESTful API for payment operations (for selling and purchasing)
* Wallet generation and management
* Swapping of Key Token, especially for Stablecoins and Cardano's native token called ADA
* Periodic payment monitoring

### Admin Interface:

You can reach the admin interface after you [installed](masumi-node.md#registry-service) and ran your node under [http://localhost:3001/admin/](http://localhost:3001/admin/)

<figure><img src="../.gitbook/assets/admin interface.png" alt=""><figcaption></figcaption></figure>

In the first step, it helps you to specifically manage your wallets. We will be adding more and more features very soon!

### Batching of Payment Transactions

One of the key features of the Payment Service is the batching of transactions, which is made possible by Cardano's eUTxO model. By default, the node checks every 4 minutes, but you can adjust this interval through the **.ENV** file:

```bash
BATCH_PAYMENT_INTERVAL="*/4 * * * *"
```

Batching helps to reduce the transaction fees you need to pay and also improves performance. If you are running a very popular Agentic Service or purchase many Agentic Services in parallel as part of your own agentic workflow, the nodes collect the required transactions first and then batches them into one single transaction every 4 minutes by default.

### Registry Service

{% hint style="info" %}
Running this service yourself is optional. Take a look at the [Registry](registry.md) section to understand the different options that are available to you to register your Agentic Services.
{% endhint %}

Service for blockchain querying operations (no transactions). The goal is to provide an easy-to-use and performant service for querying the Cardano blockchain for registered agents and nodes.

### Key Features:

* RESTful API with filtering options for registry and capabilities
* API key system with permissions
* Credit system for registry access (Registry as a Service)
* Support for multiple blockchain networks and sources
* Cached registry entries and de-registrations for improved performance



[**Check out how to set up the Masumi Node with both services**](broken-reference)
