### Hashing .#️⃣
Hashing is a process that takes an input (data) and applies a hash function to produce a fixed-size output called a hash value or hash code. Hash functions are designed to be fast and efficient, providing a unique representation of the input data. <br>


<div style="text-align:center;">
<p>

**Working of Hashing Algorithms**</p>

  ![image](https://github.com/BaibhavTiwari/100daysOfweb3/assets/75496387/8558aa73-abdc-4d83-aa05-026cdfcecb18)

</div>

The key concepts and terminologies associated with hashing are:

<b>

1. Hash Function:</b>
A hash function is a mathematical algorithm that takes an input (data) of any size and produces a fixed-size output, typically represented as a sequence of characters or bytes. The output is called a hash value or hash code. Key properties of a hash function include:

>- **Determinism:** Given the same input, a hash function will always produce the same hash value.
>- **Quick Computation:** The hash function should be computationally efficient, generating the hash value in a short amount of time.
>- **Pre-image Resistance:** It should be practically impossible to determine the original input from the hash value.
>- **Collision Resistance:** It should be highly improbable for two different inputs to produce the same hash value.

<b>

2. Hash Value/Hash Code:</b>
The output of a hash function is the hash value or hash code. It is typically a fixed-length sequence of characters or bytes. Hash values are unique representations of the input data and serve as digital fingerprints. Even a small change in the input data will produce a significantly different hash value.
<b>

3. Data Integrity:</b>
Hashing is commonly used to ensure data integrity. By comparing hash values before and after data transmission or storage, one can verify whether the data has been altered or tampered with. If the hash values match, it indicates that the data has remained unchanged.

<b>

4. Cryptographic Hash Function:</b>
Cryptographic hash functions are designed specifically for secure hashing. They are characterized by their strong collision resistance and pre-image resistance properties. Examples of cryptographic hash functions include SHA-256 (Secure Hash Algorithm 256-bit), MD5 (Message Digest Algorithm 5), and SHA-3 (Secure Hash Algorithm 3).

<b>

5. Collision:</b>
A collision occurs when two different inputs produce the same hash value. While hash functions aim for collision resistance, it is theoretically possible for collisions to occur due to the infinite number of possible inputs. However, strong cryptographic hash functions are designed to make collisions practically infeasible to find.

<b>

6. Salt:</b>
A salt is a random value added to the input data before hashing. It is used to enhance the security of hashed passwords and prevent the use of precomputed lookup tables (rainbow tables) for password cracking. Salting ensures that even identical passwords will have different hash values.

<b>

7. Rainbow Table:</b>
A rainbow table is a precomputed table of hash values and their corresponding inputs. Attackers can use rainbow tables to quickly find the original input given a hash value. Salting is used to counteract rainbow table attacks by adding uniqueness to each hashed value.

<b>

8. Merkle Tree/Hash Tree:</b>
A Merkle tree, also known as a hash tree, is a hierarchical data structure in which hash values of individual data blocks are combined to create a single root hash. It allows for efficient verification of large datasets by confirming the integrity of specific data blocks without needing to traverse the entire dataset.

###### Hashing plays a vital role in blockchain technology, ensuring data integrity, verifying transactions, creating unique identifiers for blocks and transactions, and securing the overall integrity of the blockchain. Hash functions and their properties are fundamental to the design and security of decentralized systems in Web3.0.

--------------------------------------------------------

### What is Cryptographic Hashing ❔
A cryptographic hash, also known as a cryptographic hash function, is a special type of hash designed to be secure and resistant to various types of attacks. A mathematical algorithm that takes an input (string or file) and generates a fixed-size hash value, usually represented as a string of characters or bytes.

**Deterministic:** For the same input, a cryptographic hash function will always produce the same hash value. This property ensures consistency and predictability.

**Quick Computation:** Cryptographic hash functions are designed to be computationally efficient, providing a fast and reliable way to generate hash values.

**Pre-image Resistance:** It is extremely difficult to determine the original input from the hash value. Given a hash value, it is computationally infeasible to find an input that will produce that specific hash value. This property provides a one-way function, making it practically impossible to reverse-engineer the input from the output.

**Collision Resistance:** Cryptographic hash functions aim to minimize the likelihood of two different inputs producing the same hash value (collision). While it is theoretically possible for collisions to occur due to the infinite number of possible inputs, the goal is to make collisions highly improbable to find. Strong cryptographic hash functions make it computationally infeasible to find collisions.

**Fixed Output Size:** Cryptographic hash functions produce a fixed-size output, regardless of the size of the input. For example, `SHA-256`, one of the widely used cryptographic hash functions, produces a 256-bit hash value.

###### Applications of Cryptographic Hashing:
<ul>

- `Data Integrity`

- `Password Storage`

- `Digital Signatures`

</ul>

### Cryptographic Process:
The cryptography process involves using mathematical algorithms and techniques to secure and protect sensitive information by encoding it in a way that makes it unreadable to unauthorized parties. There are two primary categories of cryptography: symmetric key cryptography and asymmetric key cryptography. Here's an overview of the cryptography process:

- Encryption:
Encryption is the process of transforming plaintext (original message) into ciphertext (encrypted message) using an encryption algorithm and a cryptographic key. There are two main types of encryption:

- Symmetric Encryption: In symmetric encryption, the same key is used for both encryption and decryption. The sender and receiver must share the secret key beforehand. The encryption algorithm takes the plaintext and the shared key to produce ciphertext. Examples of symmetric encryption algorithms include AES (Advanced Encryption Standard) and DES (Data Encryption Standard).

- Asymmetric Encryption: Asymmetric encryption, also known as public-key encryption, uses a pair of mathematically related keys: a public key and a private key. The sender uses the recipient's public key to encrypt the plaintext, and the recipient uses their private key to decrypt the ciphertext. Asymmetric encryption algorithms include RSA (Rivest-Shamir-Adleman) and Elliptic Curve Cryptography (ECC).

- Hashing:
Hashing, as explained earlier, is the process of converting an input into a fixed-size hash value using a hash function. The hash value is unique to the input, and even a small change in the input will produce a significantly different hash value. Hashing is primarily used for data integrity verification and creating digital signatures.

- Digital Signatures:
Digital signatures provide authentication, integrity, and non-repudiation of digital documents or messages. The process involves using asymmetric encryption and hashing. Here's how it works:
<ul>

- The sender computes a hash value of the message using a hash function.
- The sender encrypts the hash value using their private key, creating a digital signature.
- The digital signature is attached to the message and sent to the recipient.
- The recipient uses the sender's public key to decrypt the digital signature, obtaining the hash value.
- The recipient independently computes the hash value of the received message.
- If the computed hash value matches the decrypted hash value, the digital signature is valid, and the message is considered authentic and unaltered.
</ul>

- Key Management:
In cryptography, the secure management of cryptographic keys is crucial. Keys must be generated securely, stored safely, and exchanged securely between authorized parties. Key management involves practices such as key generation, key distribution, key storage, and key revocation to maintain the security of the cryptographic system.


- Decryption:
Decryption is the process of converting ciphertext back into plaintext using the appropriate decryption algorithm and the corresponding key. In symmetric encryption, the same key used for encryption is also used for decryption. In asymmetric encryption, the recipient uses their private key to decrypt the ciphertext received from the sender's public key encryption.