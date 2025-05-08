# Classical Encryption Techniques

## Substitution Techniques

### Caesar Cipher

- **Description**: A substitution cipher that shifts characters by a fixed number of positions in the alphabet.
- **Formula**: `C = (P + K) mod 26` (Encryption), `P = (C - K) mod 26` (Decryption)
  - `C`: Ciphertext letter
  - `P`: Plaintext letter
  - `K`: Shift value (key)
- **Encryption**:
  1. Choose a shift value (e.g., 3).
  2. Replace each letter with the letter that is `shift` positions down the alphabet.
  3. Wrap around to the beginning of the alphabet if needed.
- **Decryption**:
  1. Reverse the shift by subtracting the key value.
  2. Replace each letter with the letter that is `shift` positions up the alphabet.
  3. Wrap around to the end of the alphabet if needed.
- **Example**:
  - Plaintext: `HELLO`
  - Ciphertext (shift=3): `KHOOR`
  - Decrypted Text: `HELLO`

### Monoalphabetic Cipher

- **Description**: Each letter of the plaintext is mapped to a unique letter of the ciphertext alphabet.
- **Encryption**:
  1. Create a substitution table (e.g., A -> Q, B -> W, etc.).
  2. Replace each letter in the plaintext using the table.
- **Decryption**:
  1. Use the reverse substitution table (e.g., Q -> A, W -> B, etc.).
  2. Replace each letter in the ciphertext using the reverse table.
- **Example**:
  - Plaintext: `HELLO`
  - Ciphertext: `QWERT`
  - Decrypted Text: `HELLO`

### Playfair Cipher

- **Description**: A digraph substitution cipher using a 5x5 matrix of letters.
- **Encryption**:
  1. Create a 5x5 matrix using a keyword (e.g., `KEYWORD`).
  2. Pair up plaintext letters and apply rules for substitution.
- **Decryption**:
  1. Reverse the encryption rules to retrieve the original plaintext.
- **Example**:
  - Plaintext: `HELLO`
  - Ciphertext: `GATLM`
  - Decrypted Text: `HELLO`

### Hill Cipher

- **Description**: A polygraphic substitution cipher using linear algebra.
- **Formula**: `C = KP mod 26` (Encryption), `P = K^(-1)C mod 26` (Decryption)
  - `C`: Ciphertext vector
  - `K`: Key matrix
  - `P`: Plaintext vector
  - `K^(-1)`: Inverse of the key matrix
- **Encryption**:
  1. Represent plaintext as vectors of size `n`.
  2. Multiply by an `n x n` key matrix to get ciphertext vectors.
  3. Use modular arithmetic to ensure values are within the range of the alphabet.
- **Decryption**:
  1. Compute the inverse of the key matrix.
  2. Multiply the ciphertext vector by the inverse key matrix.
  3. Use modular arithmetic to retrieve the plaintext.
- **Example**:
  - Plaintext: `HELLO`
  - Key Matrix: `[[2, 3], [1, 4]]`
  - Ciphertext: `XMCKL`
  - Decrypted Text: `HELLO`

## Transposition Techniques

### Rail Fence Cipher

- **Description**: A transposition cipher that writes plaintext in a zigzag pattern.
- **Encryption**:
  1. Write plaintext in a zigzag pattern across multiple rows.
  2. Read off each row sequentially to form the ciphertext.
- **Decryption**:
  1. Reverse the zigzag pattern to reconstruct the original plaintext.
- **Example**:
  - Plaintext: `HELLO WORLD`
  - Ciphertext: `HOREL LWDLO`
  - Decrypted Text: `HELLO WORLD`

### Row-Column Transposition

- **Description**: Rearranges the plaintext into a grid and reads it in a different order.
- **Encryption**:
  1. Write plaintext into a grid row by row.
  2. Read off columns in a specified order to form the ciphertext.
- **Decryption**:
  1. Reverse the column order to reconstruct the original plaintext.
- **Example**:
  - Plaintext: `HELLO WORLD`
  - Ciphertext: `HLOE LWRDO`
  - Decrypted Text: `HELLO WORLD`

---

For detailed examples and images, refer to GeeksforGeeks or similar resources.
