# Generates (pseudo-)random passwords of a desired length

Generates true random passwords using /dev/urandom, with the emphasis on security over pronounceability. It can also encrypt plaintext passwords given in a temporary file.

## Manual

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

## Usage

Simply type the following command:

```
docker run rlesouef/alpine-makepasswd

```
To generate passwords with exactly 16 characters long, pass the 16 option to -l option as follows:

```
docker run rlesouef/alpine-makepasswd -l 16
```

To produce a total of 7 passwords instead of the default is one password, enter:

```
docker run rlesouef/alpine-makepasswd -l 16 -n 7
```

To generate an encrypted password:

```
docker run rlesouef/alpine-makepasswd -p mycriptpassword -e sha1
```
