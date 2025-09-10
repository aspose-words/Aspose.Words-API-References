---
title: SignatureLineOptions class
linktitle: SignatureLineOptions class
articleTitle: SignatureLineOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.SignatureLineOptions class. Allows to specify options for signature line being inserted"
type: docs
weight: 1220
url: /nodejs-net/aspose.words/signaturelineoptions/
---

## SignatureLineOptions class

Allows to specify options for signature line being inserted. Used in [DocumentBuilder](../documentbuilder/).
To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/nodejs-net/working-with-digital-signatures/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [SignatureLineOptions()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [allowComments](./allowComments/) | Gets or sets a value indicating that the signer can add comments in the Sign dialog. Default value for this property is ``false``. |
| [defaultInstructions](./defaultInstructions/) | Gets or sets a value indicating that default instructions is shown in the Sign dialog. Default value for this property is ``true``. |
| [email](./email/) | Gets or sets suggested signer's e-mail address. Default value for this property is **empty string** . |
| [instructions](./instructions/) | Gets or sets instructions to the signer that are displayed on signing the signature line. Default value for this property is **empty string** . |
| [showDate](./showDate/) | Gets or sets a value indicating that sign date is shown in the signature line. Default value for this property is ``true``. |
| [signer](./signer/) | Gets or sets suggested signer of the signature line. Default value for this property is **empty string** . |
| [signerTitle](./signerTitle/) | Gets or sets suggested signer's title. Default value for this property is **empty string** . |

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

* module [Aspose.Words](../)

