# Blockciphers_cryptography
A Block cipher is a symmetric cryptographic algorithm consisting of two paired functions:
	1.	Encryption Function (E): Converts plaintext into ciphertext.
	2.	Decryption Function (D): Converts ciphertext back into plaintext.

Core Concepts:
	•	Input Block: Fixed size  n -bit block of plaintext ( P ).
	•	Key: A secret key  K  of size  k -bits that controls the encryption and decryption processes.
	•	Output Block: An  n -bit block of ciphertext ( C ).

The encryption function is represented as:

E_K(P) = E(K, P): {0,1}^k × {0,1}^n → {0,1}^n

Here,  E_K(P)  maps a plaintext block  P  and key  K  to a ciphertext block  C .

The decryption function is the inverse of encryption:

E_K^{-1}(C) = D_K(C) = D(K, C): {0,1}^k × {0,1}^n → {0,1}^n

Decryption satisfies the property:

D_K(E_K(P)) = P

for all plaintexts  P .

Example:

For a block size of  n = 128 :
	•	Encryption: Takes a 128-bit plaintext block and produces a 128-bit ciphertext block.
	•	Decryption: Reverses the transformation using the same key.

Properties:
	•	Each key  K  defines a unique permutation (bijection) over the set of  2^n -bit blocks.
	•	The set of all possible permutations is  (2^n)! , but the key space is limited by  k , allowing  2^k  permutations.
