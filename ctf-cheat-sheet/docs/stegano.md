# Steganography

Steganography is a common CTF technique, used to hide information into a file.


## Aperi Solve

[Aperi'Solve](https://www.aperisolve.com/) is an online tool for stegano.

***

## StegCracker

[StegCracker](https://www.kali.org/tools/stegcracker/) is command line utility for cracking stegano challenges.
With StegCracker it is possible to brute-force hidden data.

### StegCracker usage

```bash
stegracker <file> <wordlist>
```
***

## Binwalk

[Binwalk](https://www.kali.org/tools/binwalk/) tool can be used to extract information and files from source.

### Binwalk usage

Extract common file types from file:
```bash
binwalk -e <file>
```

***

## Strings

Strings is a command line utility commonly found natively from *.nix operating systems.
Can be used to find information from files.

### Strings usage

Find strings from a file:
```bash
strings <file>
```
Use limiter for string length e.g. 8-character limit:
```bash
strings -n 8 <file>
```

***

## Hexdump

Hexdump can be used for extraction of binary data and files.

### Hexdump usage

Display content of a binary file with binary and text and pipe to less:
```bash
hexdump -C <file> | less
```
