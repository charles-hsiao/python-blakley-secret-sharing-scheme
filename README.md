# python-blakley-secret-sharing-scheme 

## Installation

1. Use python virtualenv(Recommand) 
```
mkvirtualenv python
```

2. Install pacakges with pip3
```
pip3 install -r requirements.txt
```

## Flow
### Encryption mode
```
1. Read a given input file (plaintext)
2. Encrypt it using AES-256 with a randomly generated 256-bit key
3. Store encrypted file (ciphertext)
4. Split the key into n parts with threshold set to k
5. Store keys to be given out
```

### Decryption mode
```
1. Read in encrypted file (ciphertext)
2. Read in the given t keys
3. Attempt to combine the keys into the original 256-bit key
4. Decrypt ciphertext with combined key using AES-256
5. Store decrypted file (plaintext) 
```

## Usage 
### Encryption
```
python3 main.py -encrypt -infile sample-txt.txt -outfile output-txt.txt -keysfile key-txt.txt -n 5 -k 3
```

### Decryption
```
python3 main.py -decrypt -infile output-txt.txt -outfile sample-txt-restored.txt -keysfile key-txt.txt
```

