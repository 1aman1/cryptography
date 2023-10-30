# TLS Handshake Process

The TLS handshake is used to establish a secure connection between a client and a server. It is commonly used in web browsers to secure HTTPS connections. The process consists of several steps:

1. **Client Hello**: The client initiates the connection by sending a "Client Hello" message to the server, including the supported TLS version, a list of supported ciphersuites, and a random value.

2. **Server Hello**: The server responds with a "Server Hello" message, selecting the TLS version, ciphersuite, and providing its own random value.

3. **Key Exchange**: The server sends its public key and, if required, a digital certificate to the client. The client verifies the server's certificate if provided and generates a pre-master secret.

4. **Client Key Exchange**: The client sends its own public key and, if necessary, a digital certificate. The server may verify the client's certificate.

5. **Finish Handshake**: Both client and server generate the session keys using the pre-master secret and exchanged values. They confirm that they are ready to start secure communication.

6. **Secure Communication**: With the session keys in place, the client and server can now encrypt and decrypt data for secure communication.
