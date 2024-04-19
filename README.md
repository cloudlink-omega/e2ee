![E2EE](https://github.com/cloudlink-omega/e2ee/assets/12957745/a2a66546-9471-4cc4-91f9-163c6917ebe5)

# E2EE
This is a Scratch 3 extension that enables E2EE (End-to-End Encryption). This E2EE extension utilizes the same underlying cryptography code that powers CloudLink Omega.

## Under the hood
This extension implements ECDH-P256-AES-GCM with SPKI-BASE64 keypairs, allowing Scratch projects to send/receive data over a wide variety of transports. It is highly resistant to attacks, and supports creating shared secrets over insecure channels (e.g. cloud variables).

## What is...

### ECDH-P256?
[Elliptic-curve Diffie–Hellman](https://en.wikipedia.org/wiki/Elliptic-curve_Diffie%E2%80%93Hellman) is a key agreement protocol that allows two parties to establish a shared encryption secret over an insecure channel. This takes advantage of a epiliptic curve keypair.

NIST P-256 is an implementation of a epiliptic curve, providing 256-bit keys that makes ECDH work.

### AES-GCM?
[Advanced Encryption Standard](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) is a symmetric encryption algorithm that utilizes public/private keys for encrypting/decrypting data. In this extension, this takes advantage of a shared key (secret), made possible by ECDH-P256.

[Galois/Counter Mode](https://en.wikipedia.org/wiki/Galois/Counter_Mode) improves performance of AES. In short, it provides authenticated encryption and integrity checking, all with great speed and low latency.

### SPKI-BASE64?
[Simple Public Key Infrastructure](https://en.wikipedia.org/wiki/Simple_public-key_infrastructure) (Pronounced Spoo-Key) simplifies linking things to keys, in favor of typical X.509-based public keys. This extension simplifies these keys into Base64 encoding that can be easily transmitted or shared.

# Disclaimers
Since Scratch does not have any concept of "secure" data storage; you should be mindful of how you store your keys. A flawed implementation of this extension can put your transmitted data at risk. 
