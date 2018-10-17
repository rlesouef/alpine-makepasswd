# Generate and encrypt passwords

Generates true random passwords using /dev/urandom, with the emphasis on security over pronounceability. It can also encrypt plaintext passwords given in a temporary file.

## Usage

```
Usage: makepasswd [-ceilMmnpSs]
       makepasswd -E [-ceilMmnSs]
  -c    String of allowed characters (A-Za-z0-9`~!@#$%^&*()-_=+)
  -E    Enumerate all possible values
  -e    Encryption algorithm (none,base64,blowfish,des,md5,sha1,sha256,shmd5)
  -i    Number of iterations in encryption algorithm
  -l    Password length
  -M    Maximum password length
  -m    Minimum password length
  -n    Number of passwords to generate
  -p    Password to use
  -S    Do not seed ourselves
  -s    Salt to use
```
