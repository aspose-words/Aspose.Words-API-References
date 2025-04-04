---
title: CertificateHolder.create method
linktitle: create method
articleTitle: create method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.DigitalSignatures.CertificateHolder.create method"
type: docs
weight: 10
url: /nodejs-net/aspose.words.digitalsignatures/certificateholder/create/
---

## create(certBytes, password) {#number[]_unknown}

Creates [CertificateHolder](../) object using byte array of PKCS12 store and its password.



```js
create(certBytes: number[], password)
```

| Parameter | Type | Description |
| --- | --- | --- |
| certBytes | number[] | A byte array that contains data from an X.509 certificate. |
| password |  | The password required to access the X.509 certificate data. |

### Returns

An instance of [CertificateHolder](../)



### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *certBytes* is``null`` |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *password* is``null`` |
| RuntimeError (Proxy error(SecurityException)) | Thrown if PKCS12 store contains no aliases |
| RuntimeError (Proxy error(IOException)) | Thrown if there is wrong password or corrupted file. |

## create(certBytes, password) {#number[]_string}

Creates [CertificateHolder](../) object using byte array of PKCS12 store and its password.



```js
create(certBytes: number[], password: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| certBytes | number[] | A byte array that contains data from an X.509 certificate. |
| password | string | The password required to access the X.509 certificate data. |

### Returns

An instance of [CertificateHolder](../)



### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *certBytes* is``null`` |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *password* is``null`` |
| RuntimeError (Proxy error(SecurityException)) | Thrown if PKCS12 store contains no aliases |
| RuntimeError (Proxy error(IOException)) | Thrown if there is wrong password or corrupted file. |

## create(fileName, password) {#string_string}

Creates [CertificateHolder](../) object using path to PKCS12 store and its password.



```js
create(fileName: string, password: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The name of a certificate file. |
| password | string | The password required to access the X.509 certificate data. |

### Returns

An instance of [CertificateHolder](../)



### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *fileName* is``null`` |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *password* is``null`` |
| RuntimeError (Proxy error(SecurityException)) | Thrown if PKCS12 store contains no aliases |
| RuntimeError (Proxy error(IOException)) | Thrown if there is wrong password or corrupted file. |

## create(fileName, password, alias) {#string_string_string}

Creates [CertificateHolder](../) object using path to PKCS12 store, its password and the alias by using which private key and certificate will be found.



```js
create(fileName: string, password: string, alias: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | string | The name of a certificate file. |
| password | string | The password required to access the X.509 certificate data. |
| alias | string | The associated alias for a certificate and its private key |

### Returns

An instance of [CertificateHolder](../)



### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *fileName* is``null`` |
| RuntimeError (Proxy error(InvalidParameterException)) | Thrown if *password* is``null`` |
| RuntimeError (Proxy error(SecurityException)) | Thrown if PKCS12 store contains no aliases |
| RuntimeError (Proxy error(IOException)) | Thrown if there is wrong password or corrupted file. |
| RuntimeError (Proxy error(SecurityException)) | Thrown if there is no private key with the given alias |

## Examples

Shows how to digitally sign documents.

```js
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw");

// Create a comment and date which will be applied with our new digital signature.
let signOptions = new aw.DigitalSignatures.SignOptions
{
  Comments = "My comment",
  SignTime = Date.now()
};

// Take an unsigned document from the local file system via a file stream,
// then create a signed copy of it determined by the filename of the output file stream.
using (Stream streamIn = new FileStream(base.myDir + "Document.docx", FileMode.open))
{
  using (Stream streamOut = new FileStream(base.artifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
  {
    aw.DigitalSignatures.DigitalSignatureUtil.sign(streamIn, streamOut, certificateHolder, signOptions);
  }
}
```

Shows how to create CertificateHolder objects.

```js
// Below are four ways of creating CertificateHolder objects.
// 1 -  Load a PKCS #12 file into a byte array and apply its password:
byte[] certBytes = File.ReadAllBytes(base.myDir + "morzal.pfx");
aw.DigitalSignatures.CertificateHolder.create(certBytes, "aw");

// 2 -  Load a PKCS #12 file into a byte array, and apply a secure password:
SecureString password = new NetworkCredential("", "aw").SecurePassword;
aw.DigitalSignatures.CertificateHolder.create(certBytes, password);

// If the certificate has private keys corresponding to aliases,
// we can use the aliases to fetch their respective keys. First, we will check for valid aliases.
using (FileStream certStream = new FileStream(base.myDir + "morzal.pfx", FileMode.open))
{
  Pkcs12Store pkcs12Store = new Pkcs12StoreBuilder().Build();
  pkcs12Store.load(certStream, "aw".ToCharArray());
  for (let currentAlias of pkcs12Store.aliases)
  {
    if ((currentAlias != null) &&
      (pkcs12Store.IsKeyEntry(currentAlias) &&
      pkcs12Store.getKey(currentAlias).Key.IsPrivate))
    {
      console.log(`Valid alias found: ${currentAlias}`);
    }
  }
}

// 3 -  Use a valid alias:
aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw", "c20be521-11ea-4976-81ed-865fbbfc9f24");

// 4 -  Pass "null" as the alias in order to use the first available alias that returns a private key:
aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw", null);
```

## See Also

* module [Aspose.Words.DigitalSignatures](../../)
* class [CertificateHolder](../)

