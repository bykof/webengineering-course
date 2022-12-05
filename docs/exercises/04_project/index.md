# Projektabgabe Pokecoin

## [Aufgabenstellung.pdf](./Projektabgabe%20Pokecoin.pdf)

# How to farm pokecoins

To farm a pokecoin you need to find the next free block in the pokecoin-blockchain.

A block in the chain is represented by a JSON, for example:

```json
{
  "previousHash": "string", // previous hash
  "data": "string", // random string
  "timestamp": 0, // milliseconds since 01.01.1970
  "nonce": 0 // random number (counts up)
}
```

It contains the previous hash, which can be received by `GET /blockchain/lastBlock` some random data, a timestamp and a nonce.
If you want to calculate the hash of your new block you need to concat the information into a single string and the information **has to be in the exact order** as shown in the example:

```js
const information =
  previousHash + timestamp.toString() + data + nonce.toString();
const hash = crypto.createHash("sha256").update(information).digest("hex");
// Result: fd884c1a84be6d4532f970cbea7baf6d5a66c8d7875d905b243d648b5b7d4f54
```

The blockchain has a difficulty, which can be received by `GET /blockchain/currentDifficulty`.
The default difficulty is 6.

This means that your hash should have a prefix of 6 zeros, to have a hash AND be unique, so no other identic hash was added to the blockchain in the past.

For example, this would be a valid hash:

```
0000001a84be6d4532f970cbea7baf6d5a66c8d7875d905b243d648b5b7d4f54
```

You can create a block with some random information and use the nonce to count up, until you receive a hash with 6 zeros for example.

Keep in mind, that while you create a new block, there could be another farmer which puts a new block onto the chain. So you have to pull the new block from the chain and use the last hash in your new block.

If you found a new block which contains the proper leading zeros, you can try to get lucky while appending the block with `POST /blockchains/blocks`.
