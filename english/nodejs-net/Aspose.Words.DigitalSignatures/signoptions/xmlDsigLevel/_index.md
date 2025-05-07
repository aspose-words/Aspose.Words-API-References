---
title: SignOptions.xmlDsigLevel property
linktitle: xmlDsigLevel property
articleTitle: xmlDsigLevel property
second_title: Aspose.Words for Node.js
description: "SignOptions.xmlDsigLevel property. Specifies the level of a digital signature based on XML-DSig standard"
type: docs
weight: 80
url: /nodejs-net/aspose.words.digitalsignatures/signoptions/xmlDsigLevel/
---

## SignOptions.xmlDsigLevel property

Specifies the level of a digital signature based on XML-DSig standard.
The default value is [XmlDsigLevel.XmlDSig](../../xmldsiglevel/#XmlDSig).



```js
get xmlDsigLevel(): Aspose.Words.DigitalSignatures.XmlDsigLevel
```

### Remarks

Different levels of XAdES signatures can be created starting from Office 2010.


### Examples

Shows how to sign document based on XML-DSig standard.

```js
let certificateHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw");
let signOptions = new aw.DigitalSignatures.SignOptions();
signOptions.xmlDsigLevel = aw.DigitalSignatures.XmlDsigLevel.XAdEsEpes;

let inputFileName = base.myDir + "Document.docx";
let outputFileName = base.artifactsDir + "DigitalSignatureUtil.xmlDsig.docx";
aw.DigitalSignatures.DigitalSignatureUtil.sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### See Also

* module [Aspose.Words.DigitalSignatures](../../)
* class [SignOptions](../)

