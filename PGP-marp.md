---
marp: true

theme: default

---
<!--- 
# First install marp-cli
sudo npm install -g @marp-team/marp-cli

# Then compile the markdown file

marp PGP-marp.md
marp PGP-marp.md --pdf
marp PGP-marp.md --pptx

--->
# Introduction to PGP (Pretty Good Privacy)
## A Guide to Secure Communication
### Presenter: Gregorio Toscano
### Date: 02/03/2025

---

# What is PGP?
- PGP stands for Pretty Good Privacy.
- It is a data encryption and decryption program for secure communication.
- Used for encrypting emails, files, and digital signatures.
- Ensures privacy, authenticity, and integrity of messages.

---

# How Does PGP Work?
- Uses **public-key cryptography** (asymmetric encryption).
- Each user has a **public key** (shared) and a **private key** (kept secret).
- **Encryption:** Sender encrypts the message with the recipient’s public key.
- **Decryption:** Recipient decrypts the message with their private key.
- Provides **authentication** using digital signatures.

---

# Installing PGP
- Download and install a PGP tool:
  - **GnuPG (GPG)** – Open-source and widely used.
  - **Kleopatra** – GUI for Windows users.
  - **PGP Tool** – Various software options available.
- Setup process:
  - Generate a key pair (public & private).
  - Store your private key securely.

---

# Generating PGP Keys
- Command-line (GPG example):
  ```sh
  gpg --full-generate-key
  ```
  1. (9) ECC (sign and encrypt) *default*
  2. (1) Curve 25519 *default*
  3. Set expiration date (optional).
  4. Enter your name and email.
  5. Set a strong passphrase.
  6. Save your keys securely.

---

# Sharing and Importing Keys
### Sharing Public Key:
  ```sh
  gpg --export -a "Your Name" > publickey.asc
  ```
  - Share it via email or key servers.
### Importing a Public Key:
  ```sh
  gpg --import publickey.asc
  ```
### Verify Key Fingerprint:
  ```sh
  gpg --fingerprint "Your Name"
  ```
  - Ensures key authenticity.

---

# Encrypting Messages & Files
### Encrypt a Message:
  ```sh
  gpg --encrypt --armor -r "Recipient Name" file.txt
  ```
  - Produces `file.txt.asc` (encrypted file).
### Encrypt a File:
  ```sh
  gpg --encrypt --recipient "Recipient Name" secret.txt
  ```

---

# Decrypting Messages & Files
### Decrypt a Message:
  ```sh
  gpg --decrypt file.txt.asc
  ```
### Decrypt a File:
  ```sh
  gpg --output decrypted.txt --decrypt secret.txt.gpg
  ```
  - Enter your private key passphrase.

---

# Digital Signatures
- Used for verifying authenticity.
### Sign a File:
  ```sh
  gpg --sign file.txt
  ```
### Verify a Signature:
  ```sh
  gpg --verify file.txt.sig
  ```

---

# Best Practices for PGP
- Keep your private key secure.
- Use a strong passphrase.
- Regularly update and revoke keys if compromised.
- Verify public keys before use.
- Backup your key pair securely.

---

# Summary
- PGP provides encryption, authentication, and integrity.
- Uses public and private keys for secure communication.
- Essential for protecting sensitive information.
- Practice safe key management and encryption techniques.

---

# Q&A
- Any questions?
- Thank you for your time!

