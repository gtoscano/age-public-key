# age-public-key
Gregorio Toscano's Age Public Key

# public key: age1cv56lf4l4yjwzt433777mehj8gdjwt3a2vq0v92r540a2jgzdfuqtlwxs9


# Introduction to Age (Actually Good Encryption)
## A Modern Approach to File Encryption
### Presenter: Gregorio Toscano
### Date: 02/03/2025

---

# What is Age?
- **Age** stands for **Actually Good Encryption**.
- A simple, modern, and secure file encryption tool.
- Designed to be a more user-friendly alternative to PGP.
- Prioritizes **ease of use** and **strong encryption** with minimal configuration.

---

# Why Use Age?
- **Simplicity:** Easy to use with straightforward commands.
- **Security:** Uses modern encryption algorithms like **X25519** and **ChaCha20-Poly1305**.
- **Portability:** Small, fast, and works across platforms.
- **No Key Management Hassles:** Generates key pairs without complex keyrings.

---

# Installing Age
### On Linux (Debian-based systems):
```sh
sudo apt install age
```

### On macOS (using Homebrew):
```sh
brew install age
```

### On Windows:
- Download the binaries from the official [Age GitHub Releases](https://github.com/FiloSottile/age/releases).

---

# Generating Age Keys
### Create a new key pair:
```sh
age-keygen -o key.txt
```
- **key.txt** contains your private key.
- Your public key will look like:
  ```
  public key: age1abcdxyz...
  ```

### Viewing your public key:
```sh
grep "# public key:" key.txt
```

---

# Encrypting Files with Age
### Encrypt a file for yourself or a recipient:
```sh
age -r age1abcdxyz... -o encrypted_file.age original_file.txt
```
- **`-r`**: Specifies the recipient's public key.
- **`-o`**: Specifies the output file name.
- **`original_file.txt`**: The file you want to encrypt.

### Encrypt with a passphrase (symmetric encryption):
```sh
age -p -o encrypted_file.age original_file.txt
```
- You'll be prompted to enter a passphrase.

---

# Decrypting Files with Age
### Decrypt a file with your private key:
```sh
age -d -i key.txt -o decrypted_file.txt encrypted_file.age
```
- **`-d`**: Decrypts the file.
- **`-i key.txt`**: Specifies your private key file.
- **`-o`**: Specifies the output (decrypted) file.

### Decrypt a passphrase-encrypted file:
```sh
age -d -o decrypted_file.txt encrypted_file.age
```
- You'll be prompted for the passphrase.

---

# Example Workflow
1. **Generate a key pair:**
   ```sh
   age-keygen -o mykey.txt
   ```
2. **Share your public key:**
   ```sh
grep "# public key:" mykey.txt
   ```
3. **Encrypt a file for yourself:**
   ```sh
   age -r age1abcdxyz... -o secret.age confidential.txt
   ```
4. **Decrypt the file:**
   ```sh
   age -d -i mykey.txt -o decrypted.txt secret.age
   ```

---

# Comparing Age and PGP
| Feature               | **PGP**                             | **Age**                         |
|-----------------------|-------------------------------------|---------------------------------|
| Key Management        | Complex keyrings, trust models      | Simple key files, no keyrings   |
| Algorithms            | RSA, DSA, ElGamal                  | X25519, ChaCha20-Poly1305       |
| Ease of Use           | Steeper learning curve              | User-friendly, minimal commands |
| File Support          | Files, emails, signatures           | File encryption only            |
| Performance           | Slower, especially with large keys  | Fast and lightweight            |

---

# Best Practices for Using Age
- **Keep your private key safe**: Store `key.txt` securely.
- **Backup your key**: If you lose it, you can't decrypt your files.
- **Use strong passphrases** for symmetric encryption.
- **Verify recipient public keys** before encrypting.

---

# Summary
- **Age** is a modern, secure, and simple alternative to PGP.
- Ideal for file encryption with minimal setup.
- Uses strong cryptographic algorithms.
- Great for quick, secure file transfers and personal encryption needs.

---

# Q&A
- Any questions?
- Thank you for your attention!

