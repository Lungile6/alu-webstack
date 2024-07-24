# General

## What are the 2 main roles of HTTPS/SSL?

The two main roles of HTTPS (Hypertext Transfer Protocol Secure) and SSL (Secure Sockets Layer) are:

1. **Authentication**: HTTPS/SSL enables the authentication of the server (and optionally the client) involved in a communication. This means that the client can verify the identity of the server it is communicating with, ensuring it is the legitimate server and not an impersonator.

2. **Encryption**: HTTPS/SSL provides encryption of the data transmitted between the client and the server. This ensures that the communication is secure and any sensitive information (such as login credentials, credit card numbers, etc.) is protected from eavesdropping and tampering.

## What is the purpose of encrypting traffic?

The primary purpose of encrypting traffic is to ensure the confidentiality and integrity of the data being transmitted. When data is encrypted, it is transformed into a coded format that can only be read by the intended recipient with the correct decryption key. This protects the data from being accessed or modified by unauthorized parties, even if they are able to intercept the communication.

Encrypting traffic is essential for securing sensitive information, such as login credentials, financial data, personal information, and other critical data that should be protected from unauthorized access or tampering. It helps prevent:

- **Eavesdropping**: Encrypted traffic is unreadable to anyone who might be monitoring the communication, making it much more difficult for attackers to steal sensitive information.

- **Man-in-the-Middle attacks**: Encryption makes it difficult for an attacker to intercept and modify the communication between the client and the server without being detected.

- **Data Tampering**: Encryption ensures that any changes made to the data during transmission will be detected, as the recipient will be unable to decrypt the modified data.

Encrypting traffic is a fundamental security measure that helps protect users' privacy and the integrity of online transactions and communications.

## What is SSL termination?

SSL termination, also known as SSL offloading, refers to the process of decrypting HTTPS/SSL-encrypted traffic at a point before it reaches the final destination server. This is typically done at a reverse proxy, load balancer, or another intermediate system, rather than at the origin server itself.

The main purposes of SSL termination are:

1. **Performance Optimization**: Decrypting the SSL/TLS traffic at an intermediate system can help offload the computational load from the origin server, which can improve the overall performance and scalability of the system.

2. **Centralized SSL/TLS Management**: SSL termination allows for centralized management and configuration of SSL/TLS certificates and settings, simplifying the process of maintaining and updating the SSL/TLS infrastructure.

3. **Enhanced Security**: SSL termination can provide an additional layer of security by inspecting the decrypted traffic for potential threats or vulnerabilities before forwarding it to the origin server.

After the SSL/TLS traffic is terminated, the unencrypted traffic is then forwarded to the origin server. In some cases, the traffic may be re-encrypted using a different SSL/TLS connection before being sent to the origin server, a process known as SSL/TLS bridging.

SSL termination is a common practice in web applications and services that handle a large volume of HTTPS/SSL-encrypted traffic, as it can help improve performance, simplify SSL/TLS management, and enhance overall security.