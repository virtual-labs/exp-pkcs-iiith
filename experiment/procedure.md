Follow these steps to explore PKCS#1 v1.5 encryption and decryption:

### Step 1: Enter Your Message

1. In the **"Plaintext to encrypt"** field, enter the text you want to encrypt
2. You can use the default "Hello World!" or enter your own message
3. Note that longer messages may require larger key sizes

### Step 2: Select or Generate RSA Keys

Choose one of the following options:

**Option A: Use Preset Keys**

- Click **"512-bit Key (e=65537)"** for a standard 512-bit key
- Click **"512-bit Key (e=3)"** for a faster encryption key with e=3
- Click **"1024-bit Key (e=65537)"** for a more secure 1024-bit key
- Click **"1024-bit Key (e=3)"** for a 1024-bit key with e=3

**Option B: Generate New Keys**

1. Set the desired key size in the **"Key size (bits)"** field (e.g., 512, 1024)
2. Click **"🔑 Generate New Key"** to create a fresh RSA key pair
3. Wait for the generation to complete (larger keys take more time)

### Step 3: Encrypt Your Message

1. Click the **"🔒 Encrypt"** button
2. Observe the encryption process in the status field
3. The encrypted ciphertext will appear in the **"Ciphertext (hex)"** field
4. Note the encryption time displayed in the status

### Step 4: Decrypt the Ciphertext

1. Click the **"🔓 Decrypt"** button
2. The decrypted message will appear in the **"Decrypted text"** field
3. Verify that it matches your original plaintext
4. Note the decryption time displayed in the status

### Step 5: Explore Key Parameters (Advanced)

1. Expand the **"Advanced Key Parameters"** section
2. Examine the various RSA key components:
   - **Modulus (n)**: The product of two prime numbers
   - **Public exponent (e)**: Used for encryption
   - **Private exponent (d)**: Used for decryption
   - **Prime factors (p, q)**: The secret primes used to generate the key
   - **CRT parameters**: Optimizations for faster decryption

### Experimental Observations

Try the following experiments:

1. **Different Key Sizes**: Compare encryption/decryption times between 512-bit and 1024-bit keys
2. **Different Exponents**: Notice the performance difference between e=3 and e=65537
3. **Message Length**: Try encrypting different length messages
4. **Error Handling**: Try decrypting without encrypting first, or modify the ciphertext

### Expected Results

- Encryption should produce a hexadecimal ciphertext
- Decryption should recover the original plaintext exactly
- Larger keys provide better security but slower performance
- The same plaintext will produce different ciphertexts due to random padding
