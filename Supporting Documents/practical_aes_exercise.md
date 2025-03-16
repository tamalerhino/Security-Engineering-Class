# Overview

**Objective:** Understand AES encryption by transforming a message using a 4x4 matrix.

**Materials Needed:**
- A 4x4 grid printed or drawn on paper (16 spaces)
- Paper and pen for writing letters
- *Optional:* Colored markers or crayons

**Background Explanation:**

In AES, messages are broken down and arranged in a 4x4 grid (matrix). This matrix is transformed in a special way so the message gets scrambled. Here, we’ll mimic a similar process to encrypt and decrypt a message.

---

## Step 1: Write a Secret Message (Plaintext)

Think of a short 16-letter message. If it’s shorter, you can fill in extra letters (like "X") at the end. For example: `"UlisesIsCool"`, which is 12 characters long. Since the matrix needs 16 slots (a 4x4 grid), add `"XXXX"` as padding at the end. The full message becomes `"UlisesIsCoolXXXX"`.

Write each letter of the message into the **4x4 matrix** starting from the top-left corner, filling left to right and top to bottom:

| U | L | I | S |
|---|---|---|---|
| E | S | I | S |
| C | O | O | L |
| X | X | X | X |

---

## Step 2: Encrypt the Message – Apply Row Shifting

AES applies several transformations. Here, we'll do **row shifts** to scramble the message:

- **Row 1:** No shift (leave as is).
- **Row 2:** Shift 1 space to the left.
- **Row 3:** Shift 2 spaces to the left.
- **Row 4:** Shift 3 spaces to the left.

After shifting, each row looks like this:
- **Row 1 (no shift):** `U L I S`  
- **Row 2 (shift 1 left):** `S I S E`  
- **Row 3 (shift 2 left):** `O L C O`  
- **Row 4 (shift 3 left):** `X X X X`

So the encrypted matrix is now:

| U | L | I | S |
|---|---|---|---|
| S | I | S | E |
| O | L | C | O |
| X | X | X | X |

This scrambled matrix represents our **encrypted message**.

---

## Step 3: Decrypt the Message – Reverse the Row Shifts

To get back the original message, reverse the shifts:

- **Row 1:** No shift.
- **Row 2:** Shift 1 space to the right.
- **Row 3:** Shift 2 spaces to the right.
- **Row 4:** Shift 3 spaces to the right.

After reversing, each row looks like this:
- **Row 1 (no shift):** `U L I S`  
- **Row 2 (shift 1 right):** `E S I S`  
- **Row 3 (shift 2 right):** `C O O L`  
- **Row 4 (shift 3 right):** `X X X X`

So the matrix returns to:

| U | L | I | S |
|---|---|---|---|
| E | S | I | S |
| C | O | O | L |
| X | X | X | X |

---

## Step 4: Read the Original Message

Reading left to right, top to bottom, the decrypted message is **"UlisesIsCoolXXXX"**, revealing **"UlisesIsCool"** as the original text!

---

## Keep in Mind: How AES Works in Real Life

In this exercise, we only shifted each row once, but **AES does this multiple times**. Real-world AES performs many rounds of shifts and other transformations to make the data nearly impossible to read without the correct key.

**Here’s how it works in real AES encryption**:

- **Key Size and Rounds**: AES can use a **128-bit, 192-bit, or 256-bit key**. The key length determines the number of rounds:
  - **128-bit key**: 10 rounds
  - **192-bit key**: 12 rounds
  - **256-bit key**: 14 rounds

- **Each Round Includes Multiple Steps**:
  - **SubBytes**: Changes each piece of data in the matrix using a substitution table (like changing letters in a code).
  - **ShiftRows**: Shifts the rows (as we did in our example).
  - **MixColumns**: Scrambles the columns to add even more complexity.
  - **AddRoundKey**: Incorporates a piece of the key into the matrix, making each round unique.

After all these rounds, the data is thoroughly scrambled, and **only the correct key** can reverse each transformation. In other words, **AES encryption is like running our row-shifting example repeatedly**, with extra steps and a powerful key guiding every transformation, making AES a highly secure method to keep data private.
