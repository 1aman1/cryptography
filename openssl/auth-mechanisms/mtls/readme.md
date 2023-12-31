# Mutual TLS (mTLS) Process

mTLS builds on the basic TLS handshake by requiring both the client and server to present digital certificates for authentication. Here's how the process works:

1. **Client Hello**: Same as in the TLS handshake, the client initiates the connection.

2. **Server Hello**: Similar to TLS, the server responds and selects the TLS version and ciphersuite.

3. **Server Certificate**: The server sends its digital certificate to the client.

4. **Client Certificate Request**: The server may request a certificate from the client.

5. **Client Certificate**: The client sends its digital certificate to the server.

6. **Key Exchange**: The key exchange and session key generation are the same as in the TLS handshake.

7. **Finish Handshake**: Similar to the TLS handshake, both parties confirm they are ready for secure communication.

8. **Secure Communication**: With the session keys in place, the client and server can communicate securely. Additionally, both parties are authenticated through their digital certificates.


# Comparison

The main difference between the TLS handshake and mTLS is that mTLS adds mutual authentication, where both the client and server authenticate each other using digital certificates. In regular TLS, only the server is authenticated (the client is typically not). In mTLS, both parties are authenticated, which adds an extra layer of security and can be useful in situations where you need to be certain of the identities of both the client and server. However, mTLS can be more complex to set up and manage due to the need for client certificates.
