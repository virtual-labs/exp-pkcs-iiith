A public-key encryption scheme consists of a set of all possible messages, called the message space **M**, and three algorithms, namely,

(a) **Gen**

(b) **Enc**

(c) **Dec**

The algorithm for key generation **Gen** is used to generate a pair of keys: a public key **pk** and a private key **sk**.

The algorithm for encryption **Enc** takes as inputs the message **m** and the public key **pk** and outputs the ciphertext **c**.

The algorithm for decryption **Dec** inputs the ciphertext **c** and the private key **sk** and outputs the message **m**.

In cryptographic practice, theoretical algorithms often require additional security measures when implemented in real-world systems. Raw or "textbook" implementations of cryptographic algorithms can be vulnerable to various attacks that exploit implementation details or mathematical properties. In cryptography, we learn that secure implementation standards and padding schemes are essential to bridge the gap between theoretical security and practical security.

**About the experiment:**

In this experiment, we work with the evolution from "textbook" RSA to secure RSA implementation following the Public-Key Cryptography Standards (PKCS v1.5). While textbook RSA demonstrates the mathematical principles of public-key cryptography, it has several vulnerabilities including deterministic encryption, malleability, and susceptibility to chosen-ciphertext attacks. PKCS v1.5 addresses these vulnerabilities through proper padding schemes and implementation guidelines. Your task is to design a secure RSA-based cryptosystem. Specifically, given an implementation of textbook RSA, you need to enhance it with PKCS v1.5 padding and understand how standardized implementation practices improve the security of cryptographic systems.
