---
title: SignOptions.signTime property
linktitle: signTime property
articleTitle: signTime property
second_title: Aspose.Words for NodeJs
description: "SignOptions.signTime property. The date of signing"
type: docs
weight: 50
url: /nodejs-net/aspose.words.digitalsignatures/signoptions/signTime/
---

## SignOptions.signTime property

The date of signing.
Default value is **current time** (datetime.datetime.now)


```js
get signTime(): Date
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

