# Overview

**Objective:** Use OpenSSL to create and verify a digital signature, understanding the role of public/private keys in proving message authenticity and integrity.

## Step 1: Generate a Private Key (for Signing)
The sender (acting as a "Signer") will create a private key. This key will be used to create a digital signature for the message.

**Generate a Private Key:**

This private key is kept secret by the sender. In real-world cases, only the authorized sender would have access to this private key.
```bash
openssl genpkey -algorithm RSA -out private_key.pem -aes256
```
## Step 2: Generate the Public Key (for Verification)
To allow others to verify the signature, the sender also needs to provide a public key that pairs with the private key.

Generate a Public Key from the private key:
```bash
openssl rsa -in private_key.pem -pubout -out public_key.pem
```

**File Summary:**

- private_key.pem: The private key used to create the digital signature (kept secret).
- public_key.pem: The public key that anyone can use to verify the signature.

## Step 3: Create a Message
The sender will now create a simple message to send to the recipient.

**Write a Sample Message:**
```bash
echo "This is a secure message from the signer." > message.txt
```

## Step 4: Create a Digital Signature
The sender uses their private key to create a digital signature for the message. This signature is unique to the message and the private key, ensuring that if either changes, the signature will no longer be valid.

**Generate a Digital Signature:**
```bash
openssl dgst -sha256 -sign private_key.pem -out signature.bin message.txt
```

**Explanation:**

- -sha256 specifies the hash function used (SHA-256).
- The signature.bin file contains the digital signature, which "locks" the message and is only valid for this specific message.

## Step 5: Share the Message and Signature(for this tutorial you dont have to share it)
The sender sends two things to the recipient:
- The original message (message.txt)
- The digital signature (signature.bin)

In real life, the recipient also needs access to the sender's public key to verify the signature.(For this tutorial you already have everything since you created the public key as well)

## Step 6: Verify the Digital Signature (Recipient Side)
The recipient now has:
- The original message
- The digital signature
- The sender’s public key

They can use this information to verify that the message is genuine and unaltered.

**Verify the Digital Signature:**
```bash
openssl dgst -sha256 -verify public_key.pem -signature signature.bin message.txt
```
If the message is authentic and hasn’t been altered, OpenSSL will output:
```bash
Verified OK
```
If the message or signature doesn’t match, OpenSSL will output an error.

## Step 7: Tamper with the Message (Optional)
To see how changes to the message affect the signature verification, you can make a slight change to message.txt (e.g., add an extra word) and re-run the verification step.

**Edit the Message:**
```bash
echo "This is a secure and verified message from the signer." > message.txt
```
**Attempt Verification Again:**
```bash
openssl dgst -sha256 -verify public_key.pem -signature signature.bin message.txt
```
This time, you’ll see an error message indicating that the verification has failed because the message was altered.

## Summary
- Digital Signature Creation: The sender used their private key to create a digital signature that uniquely represents the original message.
- Signature Verification: The recipient used the sender’s public key to verify the signature, proving the message was authentic and hadn’t been altered.
- Tamper Detection: If even a single character of the message changes, the signature no longer matches, and verification fails. This guarantees message integrity.
