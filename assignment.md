Complete the following problems to deepen your understanding of PKCS#1 v1.5 and RSA cryptography:

1. Given p = 17, q = 11, calculate N = pq = 187. If the public exponent e = 7, find the private exponent d using the extended Euclidean algorithm. Show your work step by step.

   Multiple Choice: A possible value for d is:

   - (a) 22
   - (b) 153
   - (c) 7
   - (d) 23

2. Encrypt the message m = 57 using textbook RSA with public key N = 253, e = 3. Calculate c = m^e mod N.

   Multiple Choice: The ciphertext is:

   - (a) 240
   - (b) 250
   - (c) 257
   - (d) 196

3. In asymmetric-key cryptography, the sender uses which key to encrypt a message intended for the receiver?

   Multiple Choice:

   - (a) Private key
   - (b) Public key
   - (c) Either private or public key
   - (d) None of the above

4. Explain why PKCS#1 v1.5 is more secure than textbook RSA.
   Your answer should address:
   - Padding Structure: How the padding scheme prevents predictable patterns
   - Randomness: The role of random padding in semantic security
   - Attack Prevention: Specific attacks that PKCS#1 v1.5 mitigates
   - Real-world Application: Why standards like PKCS#1 are essential for practical RSA deployment
