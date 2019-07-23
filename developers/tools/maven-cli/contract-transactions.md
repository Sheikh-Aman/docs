---
title: Contract Transactions
description: Contract transactions are the same as calls, except transactions always initiate a state-change. This means that something within the contract, like a variable, changes. This changes the state of the blockchain, which incurs a cost. Transaction calls can also change the state, or value, of something _without_ the contract having to return anything. Calls do not necessarily initiate a state-change. Calls are able to simply request the content or value of a variable. Calls will always return something, whereas contract transaction may not.
weight: 900
---

Call a transaction on a contract: `mvn aion4j:contract-txn`

## Local

Manually running a contract transaction on the local node is not possible. This is because the Aion4j plugin handles what type of call or transaction is happening. The following error is returned by the plugin when you attempt to run contract transaction on a local node:

```bash
mvn aion4j:contract-txn

> ...
> [ERROR] Failed to execute goal org.aion4j:aion4j-maven-plugin:contract-txn (default-cli) on project helloworld: For local Avm mode, use aion4j:call goal to send transaction -> [Help 1]
> ...
```

## Remote

To run a contract transaction on a remote note, run:

```bash
mvn aion4j:contract-txn -Premote
```