i used chatgpt

That screams AES-128 with a 4-digit PIN padded by 12 zeros.

Brute-forcing 0000–9999 against the first 3 blocks (48 bytes) using AES-CBC with an all-zero IV pops clean ASCII.

Result

PIN: 7352

Mode: AES-CBC with IV = 00…00 (16 zero bytes)

Decrypted plaintext / Flag:

USTCtf{01eb61687e16324487eca30736cf4d6d}
