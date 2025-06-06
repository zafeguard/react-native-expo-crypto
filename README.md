# react-native-expo-crypto

Note: this module is a clone of [crypto-browserify](https://github.com/crypto-browserify/crypto-browserify), with randombytes replaced. 

A port of node's `crypto` module to React Native.

## install

A typical workflow:

1. Install
  ```sh
  expo add expo-random && yarn add @zafeguard/react-native-expo-crypto
  ```

## the crypto in this box

What follows is unedited text from crypto-browserify

The goal of this module is to use expo-random for randombytes.

Here is the subset that is currently implemented:

* createHash (sha1, sha224, sha256, sha384, sha512, md5, rmd160)
* createHmac (sha1, sha224, sha256, sha384, sha512, md5, rmd160)
* pbkdf2
* pbkdf2Sync
* randomBytes
* pseudoRandomBytes
* createCipher (aes)
* createDecipher (aes)
* createDiffieHellman
* createSign (rsa, ecdsa)
* createVerify (rsa, ecdsa)
* createECDH (secp256k1)
* publicEncrypt/privateDecrypt (rsa)

## todo

these features from node's `crypto` are still unimplemented.

* createCredentials

these features would benefit from native implementations

* pbkdf2
* createSign
* createVerify
* createECDH
* publicEncrypto/privateDecrypt (rsa)

## contributions

If you are interested in writing a feature, please implement as a new module,
which will be incorporated into crypto-browserify as a dependency.

All deps must be compatible with node's crypto
(generate example inputs and outputs with node,
and save base64 strings inside JSON, so that tests can run in the browser.
see [sha.js](https://github.com/dominictarr/sha.js)

Crypto is _extra serious_ so please do not hesitate to review the code,
and post comments if you do.

## License

MIT
