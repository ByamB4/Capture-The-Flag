## Rivest-Shamir–Adleman

- [Brute force - encrypt 4 letter](https://github.com/ByamB4/Capture-The-Flag/blob/master/Cryptography/src/asymmetric-cipher/rsa/brute-force-encrypt-4-letter.py)
- [Brute force - encrypt e guessing](https://github.com/ByamB4/Capture-The-Flag/blob/master/Cryptography/src/asymmetric-cipher/rsa/find-e.py)
- [`c1`, `c2`, `e1`, `e2` given](https://github.com/ByamB4/Capture-The-Flag/blob/master/Cryptography/src/asymmetric-cipher/rsa/common-modules-attack.py)
- [`p`, `q`, `e` given find `d`](https://github.com/ByamB4/Capture-The-Flag/blob/master/Cryptography/src/asymmetric-cipher/rsa/p-q-e-given-calculate-d.py)
- [`N is prime`](https://github.com/ByamB4/CCC/blob/master/Cryptography/src/asymmetric-cipher/rsa/n-is-prime.py)
- [`N can be sqrt`](https://github.com/ByamB4/CCC/blob/master/Cryptography/src/asymmetric-cipher/rsa/sqrted-n.py)
- [`Three primes for two modules`](https://zeyu2001.gitbook.io/ctfs/2021/zh3ro-ctf-v2/alice_bob_dave)
- `base64 -d < pub.b64 > pub.der`
- `base64 -d priv.b64 | openssl rsa -inform DER > out.key`
- `base64 -d enc.b64 > enc`
- `openssl rsautl -decrypt -inkey out.key < enc > decrypted`

Common attacks

- `Small exponent`

  - [Find n-th root using gmpy](https://github.com/ByamB4/CCC/blob/master/Cryptography/src/asymmetric-cipher/rsa/small-exponent-attack-gmpy.py)

- `Big exponent`
  - **n** is too big then public exponent **e** must be small.
  - [Wiener's attack](https://github.com/ByamB4/CCC/blob/master/Cryptography/src/asymmetric-cipher/rsa/Wiener-Attack.py)
  - [Boneh Durfee](https://someurl)
- `Hastad’s Broadcast Attack`

  - **e** cipher text, with same **message**.
  - [Chinese remainder theorem](https://github.com/ByamB4/CCC/blob/master/Cryptography/src/asymmetric-cipher/rsa/Hastad-Broadcast-Attack-CRT.py)
  - [Simple gmpy](https://github.com/ByamB4/CCC/blob/master/Cryptography/src/asymmetric-cipher/rsa/Hastad-Broadcast-Attack-Gmpy.py)

- `Fermat's attack`

  - **p**, **q** is too near, also known as difference is small.
  - [Fermat factor](https://github.com/ByamB4/CCC/blob/master/Cryptography/src/asymmetric-cipher/rsa/Fermats-Factor-Attack-Simple.py)

- `Too many primes`

  - [Python2](https://github.com/ByamB4/Capture-The-Flag-Tools/blob/master/Cryptography/Code/rsa-too-many-primes.py)
