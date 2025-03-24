# Not-so-Simple Substitution Cipher

## Introduction
This project demonstrates an encryption algorithm based on a **Not-so-Simple Substitution** cipher, where each letter in the plaintext is shifted by an integer `n` within the range {0,1,2,...,25}. This shift serves as the encryption key, and reversing the shift decrypts the message.

## How It Works
Given a shift value `n`, each letter in the input text is replaced by a letter located `n` positions forward in the alphabet. If the shift moves past 'Z' or 'z', it wraps around to the beginning of the alphabet.

### Example (Key `n = 7`)
#### Encryption
```
Plaintext:  HELLO WORLD
Key (n):    7
Ciphertext: OLSSV DVYSK
```
#### Decryption
```
Ciphertext: OLSSV DVYSK
Key (n):    7
Plaintext:  HELLO WORLD
```

## Implementation Guide
The implementation consists of two main functions:
1. `encrypt()`: Reads plaintext from `Plaintext.txt`, encrypts it using the given shift `n`, and writes the result to `Ciphertext.txt`.
2. `decrypt()`: Reads ciphertext from `Ciphertext.txt`, decrypts it using the given shift `n`, and writes the result to `ExactPlaintext.txt`.

### Algorithm Outline
1. Read input text from `Plaintext.txt`.
2. Convert each character to its corresponding ASCII value.
3. Apply the shift `n` while ensuring that uppercase (`A-Z`) and lowercase (`a-z`) letters wrap around correctly.
4. Ignore non-alphabetic characters.
5. Write the encrypted output to `Ciphertext.txt`.
6. Read `Ciphertext.txt`, reverse the shift, and write the result to `ExactPlaintext.txt`.

## Student Task
- Implement the `encrypt()` and `decrypt()` functions in **C++, Java, or Python**.
- Ensure `encrypt()` reads from `Plaintext.txt` and writes to `Ciphertext.txt`.
- Ensure `decrypt()` reads from `Ciphertext.txt` and writes to `ExactPlaintext.txt`.
- Experiment with different values of `n`.

### Bonus Challenges
1. **Advanced Decrypt Function:**
   - Implement an `AdvancedDecrypt()` function that automatically discovers `n`.
   - It should take only `Ciphertext.txt`.
   - The function should try all possible shift values to find the correct `n`.

2. **User Interface:**
   - Add a graphical or command-line user interface for ease of use.
   - Provide options for users to input plaintext, choose `n`, encrypt, and decrypt files interactively.

### Grading System
- Base Project (Encryption & Decryption): **5 points**
- Advanced Decrypt Function: **+5 points**
- User Interface Implementation: **+5 points**

## Report Requirement
Each student must submit a report detailing:
- The programming language used (**C++, Java, or Python**).
- Step-by-step implementation of encryption and decryption functions.
- How file handling (`Plaintext.txt`, `Ciphertext.txt`, `ExactPlaintext.txt`) is managed.
- How they approached the bonus challenges (if attempted).
- Any difficulties faced and how they were solved.

## Submission Details
- Students must submit their completed project files and report.
- Send them as Cipher.YourName.zip to **sepasacademy@yahoo.com**.
- The subject of the email should be same as zip file name.
- The deadline for submission will be announced separately.

## Conclusion
This exercise helps students understand the basics of cryptography, ASCII manipulation, and modular arithmetic. Try modifying the code to explore more complex ciphers!

