---
title: SignatureLine.isSigned property
linktitle: isSigned property
articleTitle: isSigned property
second_title: Aspose.Words for NodeJs
description: "SignatureLine.isSigned property. Indicates that signature line is signed by digital signature."
type: docs
weight: 60
url: /nodejs-net/aspose.words.drawing/signatureline/isSigned/
---

## SignatureLine.isSigned property

Indicates that signature line is signed by digital signature.


```js
get isSigned(): boolean
```

### Examples

Shows how to sign a document with a personal certificate and a signature line.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let signatureLineOptions = new aw.SignatureLineOptions
{
  Signer = "vderyushev",
  SignerTitle = "QA",
  Email = "vderyushev@aspose.com",
  ShowDate = true,
  DefaultInstructions = false,
  Instructions = "Please sign here.",
  AllowComments = true
};

let signatureLine = builder.insertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.providerId = Guid.parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

expect(signatureLine.isSigned).toEqual(false);
expect(signatureLine.isValid).toEqual(false);

doc.save(base.artifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

let signOptions = new aw.DigitalSignatures.SignOptions
{
  SignatureLineId = signatureLine.id,
  ProviderId = signatureLine.providerId,
  Comments = "Document was signed by vderyushev",
  SignTime = Date.now()
};

let certHolder = aw.DigitalSignatures.CertificateHolder.create(base.myDir + "morzal.pfx", "aw");

aw.DigitalSignatures.DigitalSignatureUtil.sign(base.artifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
  base.artifactsDir + "DocumentBuilder.SignatureLineProviderId.signed.docx", certHolder, signOptions);

// Re-open our saved document, and verify that the "IsSigned" and "IsValid" properties both equal "true",
// indicating that the signature line contains a signature.
doc = new aw.Document(base.artifactsDir + "DocumentBuilder.SignatureLineProviderId.signed.docx");
let shape = (Shape)doc.getShape(0, true);
signatureLine = shape.signatureLine;

expect(signatureLine.isSigned).toEqual(true);
expect(signatureLine.isValid).toEqual(true);
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [SignatureLine](../)

