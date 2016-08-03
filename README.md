# Getting Started with Cryptography in Python

#### Crypto & Privacy Village (DEFCON 24), 2016

[Amirali Sanatinia](http://www.ccs.neu.edu/home/amirali)


Today we use cryptography in almost everywhere. From surfing the web over
https, to working remotely over ssh. However, many of us do not appreciate
the subtleties of crypto primitives, and the lack of correct and updated
resources leads to design and development of vulnerable applications. In
this talk, we cover the building block of modern crypto, and how to develop
secure applications in Python.


## Requirements

 * Python 2.6+
 * [Jupyter Notebook](http://jupyter.org/)
 * [cryptography](http://cryptography.io/)


## OpenSSL

To create *RSA* key pairs you can use the following commands:

```
$ openssl genrsa -out private_key.pem 2048
$ openssl pkcs8 -topk8 -inform PEM -outform DER -in private_key.pem -out private_key.der -nocrypt
$ openssl rsa -in private_key.pem -pubout -outform DER -out public_key.der
