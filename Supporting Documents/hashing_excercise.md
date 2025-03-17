# Overview
Understand how hashing works by creating hash values for different inputs and observing how even small changes lead to different hashes.

## Step 1: Generate a Hash for Simple Text
1. Go to CyberChef.
2. In the left "Recipe" panel, add the **SHA-2** operation by searching for "SHA-2" and clicking on it, set the "size" to "256".
3. In the input panel, enter a simple word like "Hello".
4. Observe the output in the right panel, which shows the SHA2(SHA-256) hash for **"Hello"**.

## Step 2: Modify the Input and Observe the Change in Hash
1. Change the input slightly by adding a period, making the input **"Hello."**.
2. Observe how the SHA-256 hash output changes completely, even though only one character was added.

Even a small change in the input leads to a drastically different hash, demonstrating the **avalanche effect** in hashing.

## Step 3: Hash a Larger Text
1. Enter a sentence like **"The quick brown fox jumps over the lazy dog"**.
2. Observe the SHA-256 hash generated.

## Step 4: Demonstrate Hash Consistency
Clear the input panel, then re-enter **"Hello"** exactly as before.

Verify that the *SHA-256* hash output is identical to the first hash generated for **"Hello"**.

Hash functions are **deterministic** — the same input will always produce the same hash.

# Summery 
- Deterministic Nature of Hashing: The same input always generates the same hash.
- Avalanche Effect: Small changes in input result in completely different hashes.
- Uniqueness: Hashes provide a unique fingerprint for data, making them useful for verifying data integrity.
