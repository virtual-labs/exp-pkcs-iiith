Follow these steps to explore PKCS#1 v1.5 RSA encryption and decryption using the interactive simulation:

### **Phase 1: Message Input and Initial Setup**

**STEP 1:** Enter your message in the plaintext field

- Type your desired message in the **"Plaintext to encrypt"** field
- You can use the default "Hello World!" or enter your own text
- Consider that longer messages may require larger key sizes for proper encryption

**STEP 2:** Observe the simulation interface organization

- **Step 1 Section (Yellow)**: Message encryption/decryption operations
- **Step 2 Section (Green)**: RSA key management and parameters
- **Advanced Section (Red)**: Detailed key parameters for cryptographic analysis

### **Phase 2: RSA Key Selection and Management**

**STEP 3:** Choose your RSA key configuration from the preset options:

- **Green Button - 1024-bit Key (e=65537)**: Standard secure key with common public exponent
- **Orange Button - 1024-bit Key (e=3)**: Fast encryption key with small public exponent
- **Red Button - 512-bit Key (e=65537)**: Smaller key for faster operations
- **Purple Button - 512-bit Key (e=3)**: Fastest encryption with minimal security trade-off

**STEP 4:** OR generate a custom RSA key:

- Set your desired key size in the **"Key size (bits)"** field (512, 1024, or larger)
- Click the **"🔑 Generate New Key"** button (cyan/blue)
- Wait for the generation process to complete (larger keys require more time)

**STEP 5:** Examine the generated key parameters:

- **Modulus (n)**: The public modulus used in both encryption and decryption
- **Public Exponent (e)**: The public key component (typically 65537 or 3)
- **Private Exponent (d)**: The secret key component for decryption

### **Phase 3: Encryption and Decryption Operations**

**STEP 6:** Perform PKCS#1 v1.5 encryption:

- Click the **"🔒 Encrypt"** button (green) in the message operations section
- Observe the encryption process in the status field
- The ciphertext appears in hexadecimal format in the **"Ciphertext (hex)"** field
- Note the encryption time and any status messages

**STEP 7:** Perform decryption to verify the process:

- Click the **"🔓 Decrypt"** button (orange) to reverse the encryption
- The decrypted message appears in the **"Decrypted text"** field
- Verify that the decrypted text exactly matches your original plaintext
- Observe the decryption time in the status field

### **Phase 4: Advanced Cryptographic Analysis**

**STEP 8:** Explore advanced RSA parameters (optional):

- Click to expand the **"Advanced Key Parameters"** section (red background)
- Examine the mathematical components:
  - **Prime Factors (P, Q)**: The secret primes that generate the modulus
  - **D mod (P-1)**: Chinese Remainder Theorem optimization parameter
  - **D mod (Q-1)**: CRT parameter for faster decryption
  - **1/Q mod P**: CRT coefficient for reconstruction

**STEP 9:** Conduct comparative experiments:

- **Key Size Comparison**: Generate keys of different sizes and compare performance
- **Exponent Analysis**: Compare encryption speed between e=3 and e=65537
- **Security vs Performance**: Observe the trade-off between key size and operation speed
- **Padding Verification**: Notice how the same plaintext produces different ciphertexts due to random padding
