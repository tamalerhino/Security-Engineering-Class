# Overview
**Objective:** Use OpenSSL to simulate a TLS handshake and secure communication, understanding the key components like certificate creation, encryption, and decryption.

## Step 1: Generate a Self-Signed Certificate for the "Server"
In a real TLS setup, the server has a digital certificate signed by a trusted authority. Here, we’ll create a self-signed certificate, which acts like a temporary certificate for our server.

**Generate a Private Key for the server:**

This command creates a **private key** with 256-bit AES encryption.
```bash
openssl genpkey -algorithm RSA -out server_key.pem -aes256
```
**Create a Self-Signed Certificate using the private key:**

This command creates a **cert** signed with your private key
```bash
openssl req -new -x509 -key server_key.pem -out server_cert.pem -days 365
```
Follow the prompts to enter information for the certificate, such as "Common Name" (e.g., “localhost” or your server name). The certificate will be valid for 365 days.

**File Summary:**
- server_key.pem: Server’s private key.
- server_cert.pem: Server’s self-signed certificate, containing the public key.

## Step 2: Simulate a "Client" Verifying the Server’s Certificate
View the Server’s Certificate: The client would normally verify the server’s certificate. Here, we’ll display it to examine the contents. 
```bash
openssl x509 -in server_cert.pem -text -noout
```
This step allows you to inspect details of the certificate, like issuer information and the public key.

## Step 3: Encrypt a Message (Simulate Secure Communication)
Now, we’ll use the server’s **public key** to encrypt a message, similar to how a **client encrypts** a session key for secure communication.

Create a Sample Message in **Plain-Text**:
```bash
echo "Hello, this is a secure message!" > message.txt
```
**Encrypt** the Message(plain-text) with the server’s **public key**:
```bash
openssl rsautl -encrypt -inkey server_cert.pem -pubin public_key.pem -in message.txt -out encrypted_message.bin
```
This step simulates the client sending an encrypted message that only the server can decrypt using its private key.

## Step 4: Decrypt the Message on the Server Side
The server will now decrypt the message using its private key, simulating how TLS uses asymmetric encryption to establish secure communication.

**Decrypt** the Message with the server’s private key:
```bash
openssl rsautl -decrypt -inkey server_key.pem -in encrypted_message.bin -out decrypted_message.txt
```
**View the Decrypted Message:**
```bash
cat decrypted_message.txt
```
You should see the original message: **"Hello, this is a secure message!"**

## Step 5: (Optional) Generate a Symmetric Key and Encrypt with AES
To simulate the switch to symmetric encryption (as TLS does after the handshake), you can create an AES key and use it to encrypt/decrypt messages.

**Generate a 256-bit AES Key:**
```bash
openssl rand -hex 32 > symmetric_key.bin
```
**Encrypt the Message Using AES:**
```bash
openssl enc -aes-256-cbc -salt -in message.txt -out message_aes.enc -pass file:./symmetric_key.bin
```
**Decrypt the Message Using AES:**
```bash
openssl enc -d -aes-256-cbc -in message_aes.enc -out decrypted_message_aes.txt -pass file:./symmetric_key.bin
```
**Check the Decrypted Message:**
```bash
cat decrypted_message_aes.txt
```

## Summary of What We Simulated
- Certificate Creation: The server created a certificate, allowing the client to verify the server’s identity.
- Asymmetric Encryption: The client encrypted a message using the server’s public key, which only the server could decrypt with its private key.
- Symmetric Key Encryption (Optional): We created a symmetric AES key, encrypted the message, and decrypted it with the same key, just like TLS does after establishing a session.
