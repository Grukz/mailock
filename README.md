###This project is NOT being maintained.
> If you have any questions please email me at [gmontalvo@protonmail.com](mailto:gmontalvo@protonmail.com)

# mailock

[![npm version](https://img.shields.io/npm/v/mailock.svg?style=flat)](https://www.npmjs.com/package/mailock) 
[![Dependency Status](https://david-dm.org/gmontalvoriv/mailock.svg)](https://www.npmjs.com/package/mailock)
[![npm downloads](https://img.shields.io/npm/dt/mailock.svg?style=flat)](https://www.npmjs.com/package/mailock)

#### A command-line utility to send encrypted emails via SMTP with OpenPGP.js and Nodemailer.
`mailock` is a simple command-line utility that lets you encrypt and decrypt your files, sign and verify your messages, and send out content securely through SMTP using the Nodemailer library. Taking advantage of Node.js's great cross-platform support, this project aims to make use of these libraries and making standard PGP encryption services available in one package.

## Installation

`npm install -g mailock`

## Key Pair generation

Generate your private and public keys.

`mailock --keygen`

## Encryption

`mailock encrypt receiver@someserver.com plaintextFile`

## Decryption

`mailock decrypt user@someserver.com encryptedMessage`

## Message authentication and integrity checking

#### Sign your message

`mailock sign user@someserver.com messagefile`

#### Verify signature

`mailock verify user@someserver.com message`

Returns _true_ if signature validation is successful.

## Third party libraries

All of the project's file security methods are done using the [OpenPGP.js](http://openpgpjs.org) library, and email service with [Nodemailer](http://nodemailer.com/).

For more information on how these libraries work, please check out their GitHub pages:

* [OpenPGP.js](https://github.com/openpgpjs/openpgpjs)
* [Nodemailer](https://github.com/andris9/Nodemailer)
