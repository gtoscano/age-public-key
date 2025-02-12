# Public Keys of Gregorio Toscano (gtoscano)

Welcome to my public keys repository. Here, I share my public keys for secure communications and file encryption.

## About Me

- **Name:** Gregorio Toscano
- **GitHub Username:** [gtoscano](https://github.com/gtoscano)

## Available Public Keys

### AGE Public Key

- **File:** `gtoscano-pulic-key.txt`
- **Key:**

  ```
  # public key: age1cv56lf4l4yjwzt433777mehj8gdjwt3a2vq0v92r540a2jgzdfuqtlwxs9
  ```

This key can be used with the [age encryption tool](https://github.com/FiloSottile/age). To encrypt a file for me using age, you can run:

```bash
age -r age1cv56lf4l4yjwzt433777mehj8gdjwt3a2vq0v92r540a2jgzdfuqtlwxs9 -o encrypted.age yourfile.txt
```

### PGP Public Key

- **File:** `gtoscano-pgp-publickey.asc`
- **Key:**

  ```
  -----BEGIN PGP PUBLIC KEY BLOCK-----

  mDMEZ6z8WhYJKwYBBAHaRw8BAQdAVdxqGfbfeSZGzYIGx1Won4VmZgj9zYQ1xk9q
  UBQAAP+0JUdyZWdvcmlvIFRvc2Nhbm8gPGd0b3NjYW5vQGdtYWlsLmNvbT6IkwQT
  FgoAOxYhBG2IIdgEM7AL0PpS/UrwYF99ORT6BQJnrPxaAhsDBQsJCAcCAiICBhUK
  CQgLAgQWAgMBAh4HAheAAAoJEErwYF99ORT6VsABAJhVvHejRtK2vr91XnwPWS8M
  TJGXj1RHqc57g1GdWmaFAP9zHE04jH/JJkaVscpn6XTJVupl9IZdUAJndpMdDl4m
  Abg4BGes/FoSCisGAQQBl1UBBQEBB0AAx2cTPrxe0btk5nzy09h7qyeFwsvP/eph
  JLK3ed5XRQMBCAeIeAQYFgoAIBYhBG2IIdgEM7AL0PpS/UrwYF99ORT6BQJnrPxa
  AhsMAAoJEErwYF99ORT6wSABAP1HwaXjVbvuXHaf5KAfewsbcCrNLRk8W5PTIu/b
  6kJmAPsEFOnvsgVTcilDuqWgH87RieSPrdHv/ot5uGq28QdiBQ==
  =J3Ao
  -----END PGP PUBLIC KEY BLOCK-----
  ```

This key is intended for use with PGP-compatible tools such as [GnuPG](https://gnupg.org/). To import my PGP key, run:

```bash
gpg --import gtoscano-pgp-publickey.asc
```

## How to Use These Keys

- **For AGE Encryption:**  
  Use my AGE public key to encrypt files meant for me. The encryption command explicitly specifies the recipient's public key as shown above.

- **For PGP Encryption:**  
  Import my PGP public key to your keyring and use it for encrypting emails or files. Consult your PGP tool's documentation for further details.

## Contact

If you have any questions or need assistance with secure communications, feel free to open an issue or contact me directly.

---

*This repository is maintained by Gregorio Toscano (gtoscano).*
