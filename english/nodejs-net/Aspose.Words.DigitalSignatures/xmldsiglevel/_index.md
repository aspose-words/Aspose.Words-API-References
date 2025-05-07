---
title: XmlDsigLevel enumeration
linktitle: XmlDsigLevel enumeration
articleTitle: XmlDsigLevel enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.DigitalSignatures.XmlDsigLevel enumeration. Specifies the level of a digital signature based on XML-DSig standard."
type: docs
weight: 60
url: /nodejs-net/aspose.words.digitalsignatures/xmldsiglevel/
---

## XmlDsigLevel enumeration

Specifies the level of a digital signature based on XML-DSig standard.


### Members

| Name | Description |
| --- | --- |
| XmlDSig | Specifies XML-DSig signature level. |
| XAdEsEpes | Specifies XAdES-EPES signature level. |

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

* module [Aspose.Words.DigitalSignatures](../)

