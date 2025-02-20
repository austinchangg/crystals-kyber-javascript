# CRYSTALS-KYBER JavaScript

<p align="center">
  <img src="./kyber.png"/>
</p>

**CRYSTALS-KYBER** is a post-quantum key exchange protocol.

This protocol is used to securely establish symmetric keys between two parties. 

This JavaScript implementation is intended for client-side web browser applications and server-side backends in Node.js frameworks.

Most of this code was translated from a Go implementation of Kyber which can be found [here](https://github.com/symbolicsoft/kyber-k2so).

Original code (written in C) can be found [here](https://github.com/pq-crystals/kyber).

Kyber comes in 512, 768, 1024 security strengths.

This code is the most up to date version based off the [NIST PQC Round 3 Submissions](https://csrc.nist.gov/projects/post-quantum-cryptography/round-3-submissions).

## Functionality

**KYBER** will securely distribute a 256 bit symmetric key between two parties. To safely transmit data over a channel using the key, an AEAD is advised (such as AES-256-GCM).

The exchange can be visualised below:

![](./diagram.svg)

## Usage
Using Node.js (v16.17.0) or React:
```bash
npm install
```

## Running Tests
```js
node index.js
```
Output from function `kyber.Test768()` that tests compatibility with the C implementation based on run cases in `PQCkemKAT_2400.rsp`.
```
Test run [ 0 ] success
Test run [ 1 ] success
Test run [ 2 ] success
Test run [ 3 ] success
Test run [ 4 ] success
Test run [ 5 ] success
          .
          .
          .
Test run [ 95 ] success
Test run [ 96 ] success
Test run [ 97 ] success
Test run [ 98 ] success
Test run [ 99 ] success
 
All test runs successful.

ss1 <Buffer cd c4 7d 83 2b 49 5d 82 3c 08 34 ea 12 f0 4a 8f 5c 4c d6 19 b1 79 85 71 d6 b2 a7 c9 3f ac cc d1>
ss2 <Buffer cd c4 7d 83 2b 49 5d 82 3c 08 34 ea 12 f0 4a 8f 5c 4c d6 19 b1 79 85 71 d6 b2 a7 c9 3f ac cc d1>
1
```

## Further Information
More details about CRYSTALS-KYBER, lattice-based cryptography and a real-life use of this algorithm can be
read here [Active Implementation of Post-Quantum End-to-End Encryption](https://eprint.iacr.org/2021/356.pdf) [20 Apr 2021].
