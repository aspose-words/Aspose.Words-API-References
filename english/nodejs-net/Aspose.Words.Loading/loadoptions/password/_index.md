---
title: LoadOptions.password property
linktitle: password property
articleTitle: password property
second_title: Aspose.Words for NodeJs
description: "LoadOptions.password property. Gets or sets the password for opening an encrypted document"
type: docs
weight: 110
url: /nodejs-net/aspose.words.loading/loadoptions/password/
---

## LoadOptions.password property

Gets or sets the password for opening an encrypted document.
Can be ``null`` or empty string. Default is ``null``.



```js
get password(): string
```

### Remarks

You need to know the password to open an encrypted document. If the document is not encrypted, set this to ``null`` or empty string.




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

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

