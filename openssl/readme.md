# Cryptography

Cryptography is the art of securing plain text in a way that cannot be easily understood by any party other than the SENDER and RECEIVER.

There are multiple ways to achieve this:

## Caesar Cipher

A basic method for encoding plain text is the Caesar cipher, also known as a substitution cipher. In this method, each letter is shifted by a fixed amount:

- A -> B
- M -> N
- N -> O

While this is a simple form of encryption, it's not very secure. For example:

- "Vikas" becomes "Wjlbt"

## Block Cipher

Block ciphers provide more security compared to single character substitution. Instead of shifting individual characters, a block of characters is manipulated, adding complexity to the encryption process. For example:

- "AMAN GUPT A000" becomes "ANYS UITA BLEA LGOR ITHM"

Note: In reality, the characters can be swapped with Unicode characters (16 bits), making decryption more challenging.

## Content

Here's what you can find in the videos:

- 1: Symmetric encryption
- 2: Asymmetric encryption, digital signature (tamper evident)
- 3: Digital certificates
- 5: TLS establishment
- 7: mTLS

## Encryption Types

There are two main encryption types:

### Symmetric

- Key pair driven
- Same/symmetric key pair
- Same algorithm for encryption/decryption
- Efficient computation
- Keys must be shared, which becomes a serious concern as the number of parties involved in the exchange increases.

### Asymmetric

- Key pair driven
- Different key pair
- Different algorithms for encryption/decryption
- Requires more computation
- Keys are easier to share due to the public-private key concept unique to asymmetric encryption

Real-world implementations often use hybrid approaches for the best balance of security and performance. Common algorithms include AES and RSA.

## Digital Signature

Digital signatures are used to verify the authenticity and integrity of digital messages or documents. They function similarly to handwritten signatures on physical documents but in the context of electronic communication and data.

The process involves:

1. Calculating a message digest (hash) of the content to sign.
2. Encrypting the message digest with the sender's private key to create a digital signature.
3. Sending both the original message and the digital signature to the recipient.
4. The recipient calculates a new message digest of the received message.
5. The recipient uses the sender's public key to decrypt the digital signature. If the decrypted signature matches the calculated message digest, it confirms that the message hasn't been altered in transit.

## Digital Certificates

certificate authority signs a certificate using it's private key.

a certificate is for demonstrating that THIS-id is bound to THIS-entity, like an IDcard.
IDcard's reliability is as good as the source of IDcard issuer, the entity who issued that card.
Analogous to this situation, the issuer is CA certificate Authority.

## Over to Terminal

NOTE – it all starts with the PRIVATE key

To be continued...
