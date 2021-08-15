# Send me an encrypted file using GPG public key

- Install gpg2

On Ubuntu/Debian based Linux OS

`sudo apt install gpg2`

On RHEL based Linux OS

`sudo yum install gpg2`

On Windows OS

`Download GPG executable from https://www.gpg4win.org/ and install it.`

- Download public key from keyserver.

https://pgp.mit.edu/pks/lookup?op=get&search=0xF4AD41E882AE97BE


- Import the public key from downloaded public key.

`gpg2 --import file_public.key

- OR you can import directly from keyserver using below command.

`gpg2 --keyserver pgp.mit.edu --recv-keys F4AD41E882AE97BE`

- Encrypt file

`gpg2 --encrypt --sign --armor -r navratan.gupta@protonmail.com file_to_encrypt`

- A file will be created with file_to_encrypt.asc.
- Attach the same file to email along with your GPG public key so that I can reply you back in encrypted mail.


# Decrypt an PGP encrypted file

- Import private key, if not already in GPG keyring.

`gpg2 --import private.key`

- Decrypt file

`gpg --decrpt encrypted_file.asc`
