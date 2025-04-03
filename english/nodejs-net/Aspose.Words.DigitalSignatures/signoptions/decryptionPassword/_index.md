---
title: SignOptions.decryptionPassword property
linktitle: decryptionPassword property
articleTitle: decryptionPassword property
second_title: Aspose.Words for NodeJs
description: "SignOptions.decryptionPassword property. The password to decrypt source document"
type: docs
weight: 30
url: /nodejs-net/aspose.words.digitalsignatures/signoptions/decryptionPassword/
---

## SignOptions.decryptionPassword property

The password to decrypt source document.
Default value is **empty string** ().



```js
get decryptionPassword(): string
```

### Remarks

If OOXML document is encrypted, you should provide decryption password
to decrypt source document before it will be signed.
This is not required for documents in binary DOC format.


### Examples

Shows how to sign encrypted document file.

```js
// Create an X.509 certificate from a PKCS#12 store, which should contain a private key.
let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw");

// Create a comment, date, and decryption password which will be applied with our new digital signature.
let signOptions = new aw.DigitalSignatures.SignOptions
{
  Comments = "Comment",
  SignTime = Date.now(),
  DecryptionPassword = "docPassword"
};

// Set a local system filename for the unsigned input document, and an output filename for its new digitally signed copy.
string inputFileName = base.myDir + "Encrypted.docx";
string outputFileName = base.artifactsDir + "DigitalSignatureUtil.decryptionPassword.docx";

aw.DigitalSignatures.DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### See Also

* module [Aspose.Words.DigitalSignatures](../../)
* class [SignOptions](../)

