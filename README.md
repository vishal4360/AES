# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```
def simple_aes_encrypt(plaintext, key):
    ciphertext = []
    klen = len(key)

    for i in range(len(plaintext)):
        ciphertext.append(ord(plaintext[i]) ^ ord(key[i % klen]))

    return ciphertext
def simple_aes_decrypt(ciphertext, key):
    decrypted_text = ""
    klen = len(key)

    for i in range(len(ciphertext)):
        decrypted_text += chr(ciphertext[i] ^ ord(key[i % klen]))

    return decrypted_text
def print_ascii(ciphertext):
    print("Encrypted Message (ASCII values): ", end="")
    for value in ciphertext:
        print(value, end=" ")
    print()

plaintext = input("Enter the plaintext: ")
key = input("Enter the key: ")
if len(key) == 0:
    print("Error: Key cannot be empty!")
    exit()

ciphertext = simple_aes_encrypt(plaintext, key)
print_ascii(ciphertext)
decrypted_text = simple_aes_decrypt(ciphertext, key)
print("Decrypted Message:", decrypted_text)
```

# OUTPUT:
<img width="1617" height="808" alt="Screenshot 2026-08-05 105811" src="https://github.com/user-attachments/assets/48ea1c83-b3e0-4360-9e5d-d15f987b19b1" />




# RESULT:
The program is successfully implemented and executed successfully


