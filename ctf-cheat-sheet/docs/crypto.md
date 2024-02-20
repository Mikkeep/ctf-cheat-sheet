# Cryptography Challenges

## Openssl

### Openssl usage

***

## John the Ripper

John the Ripper can be used to bruteforce passwords.

### John the Ripper usage

#### PDF file bruteforce
Turn the pdf file to usable with John.
```bash
pdf2john <pdf_file_here> <output_hashfile_name_here>
```

Brute the generated file with John:

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt <output_hashfile_name_here>
```

***

## Hashcat

Hashcat can be used to bruteforce passwords and to generate mutations from words.

Rule for case toggling can be found [here](https://hashcat.net/wiki/doku.php?id=toggle_attack_with_rules)
Custom rules can be inserted into a file and used.

### Hashcat usage

Mutate a word or wordlist:

Create a wordlist, e.g. ```echo "Bob" > wordlist.txt```

Then use this wordlist for mutation from Hashcats pre shipped rule:

```bash
hashcat --force --stdout wordlist.txt -r /usr/share/hashcat/rules/leetspeak.rule > leet_wordlist.txt
```
Same can be done for custom rules, just replace the rule file.

***

## CyberChef

Access CyberChef [from here](https://gchq.github.io/CyberChef/)
