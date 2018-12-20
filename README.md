# RSA

OVERVIEW
--------------------------------------------------
This is an implementation of a RSA algorithm to study cryptography for the [Security Engineering] course. It was made at the Computer Science undergraduate program from University of São Paulo (ICMC - USP).

HOW DOES RSA WORK?
--------------------------------------------------
RSA involves a pair of keys: a public key, which can be known by all, and a private key, which must be kept secret. Any message encrypted using a public key can only be decrypted using its private key.
The idea of RSA is based on the fact that it is difficult to factorize a large integer value. The public key consists of two numbers, where one of the values is the multiplication of two prime numbers. The private key is also obtained through these two prime numbers. The strength of the encryption is based on the value of the key, so if this value is doubled or tripled, the strength of the encryption increases exponentially. RSA keys usually have a size of 1024 or 2048 bits.

* Public key:  n = P * Q, where 'P' and 'Q' are distinct prime numbers.
* Private key: d = ((k * phi (n) + 1) / e), where 'e' is the encrypting exponent.

HOW TO COMPILE
--------------------------------------------------
```bash
   1. Clone repository: https://github.com/wesjrock/EngSegCripto.git
   2. python main.py [e|d] [input_file]
   
   e: to encrypt
   d: to decrypt
   
   Examples:
   * encryption: python main.py e my_text.txt
   * decryption: python main.py d encrypted.txt
   
```

LIMITATIONS
--------------------------------------------------
Time and processing, this implementation accepts only text format files as input. The text file can not display ASCII 221 or higher characters because of language limitation (variable overflow occurs when large generator numbers are chosen).

MORE INFO
--------------------------------------------------
You can find more information about the project in the file:  `project report.pdf`
* RSA <https://en.wikipedia.org/wiki/RSA_(cryptosystem)>
