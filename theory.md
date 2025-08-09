PKCS#1 v1.5 (Public-Key Cryptography Standards #1 version 1.5) is a padding scheme used with RSA encryption to provide security against certain attacks. It was developed by RSA Security Inc. and is widely used in various cryptographic applications.

#### RSA Algorithm Overview

RSA is an asymmetric cryptographic algorithm that uses a pair of keys:

- **Public Key**: Used for encryption, consists of modulus (n) and public exponent (e)
- **Private Key**: Used for decryption, consists of modulus (n) and private exponent (d)

#### Key Generation

1. Choose two large prime numbers p and q
2. Compute n = p × q (the modulus)
3. Compute φ(n) = (p-1) × (q-1) (Euler's totient function)
4. Choose e such that 1 < e < φ(n) and gcd(e, φ(n)) = 1
5. Compute d ≡ e⁻¹ (mod φ(n)) (the private exponent)

#### PKCS#1 v1.5 Padding

Before encryption, the message is padded according to PKCS#1 v1.5 format:

```
0x00 || 0x02 || PS || 0x00 || M
```

Where:

- **0x00**: Leading zero byte
- **0x02**: Block type for encryption
- **PS**: Padding string of random non-zero bytes (at least 8 bytes)
- **0x00**: Separator
- **M**: The actual message

#### Encryption Process

1. Apply PKCS#1 v1.5 padding to the message
2. Convert the padded message to an integer
3. Compute ciphertext = message^e mod n

#### Decryption Process

1. Compute message = ciphertext^d mod n
2. Remove PKCS#1 v1.5 padding
3. Extract the original message

#### Security Features

- **Randomness**: The padding string PS contains random bytes, making each encryption unique
- **Structure**: The fixed format helps detect errors and prevents certain attacks
- **Length**: Ensures the padded message is the same length as the modulus

#### Common Key Sizes and Exponents

- **512-bit keys**: Fast but less secure, suitable for educational purposes
- **1024-bit keys**: More secure, commonly used in practice
- **Public exponent e=3**: Fast encryption but requires careful implementation
- **Public exponent e=65537 (0x10001)**: Good balance of security and performance

For a detailed mathematical analysis, refer to the [PKCS#1 specification](docs/PKCS1.pdf).

<img src="images/image10.png" alt="PKCS#1 v1.5 Encryption Scheme Diagram"/>
