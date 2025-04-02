---
title: SignOptions.comments property
linktitle: comments property
articleTitle: comments property
second_title: Aspose.Words for NodeJs
description: "SignOptions.comments property. Specifies comments on the digital signature"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.DigitalSignatures/signoptions/comments/
---

## SignOptions.comments property

Specifies comments on the digital signature.
Default value is **empty string**().



```js
get comments(): string
```

### Examples

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

### See Also

* module [Aspose.Words.DigitalSignatures](../../)
* class [SignOptions](../)

