mbedtls-csrp
============
Derived from https://github.com/cocagne/csrp

mbedtls-csrp is a minimal C implementation of the [Secure Remote Password
protocol](http://srp.stanford.edu/). The project consists of a single
C file and is intended for direct inclusion into utilizing programs. 
It's only dependency is mbedtls (https://github.com/ARMmbed/mbedtls).

SRP Overview
------------

SRP is a cryptographically strong authentication
protocol for password-based, mutual authentication over an insecure
network connection.

Unlike other common challenge-response autentication protocols, such
as Kereros and SSL, SRP does not rely on an external infrastructure
of trusted key servers or certificate management. Instead, SRP server
applications use verification keys derived from each user's password
to determine the authenticity of a network connection.

SRP provides mutual-authentication in that successful authentication
requires both sides of the connection to have knowledge of the
user's password. If the client side lacks the user's password or the
server side lacks the proper verification key, the authentication will
fail.

Unlike SSL, SRP does not directly encrypt all data flowing through
the authenticated connection. However, successful authentication does
result in a cryptographically strong shared key that can be used
for symmetric-key encryption.


